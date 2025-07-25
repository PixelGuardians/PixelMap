# Pixel Map

## Structure

A Pixel Map (.pxl) file consists of two sections:

- YAML Frontmatter (required)
  - Pixel Keys (required)
- Pixel Mapping (required)

## YAML Frontmatter

The frontmatter must be located at the very beginning of the file and is delimited by triple dashes `---`.
The frontmatter must include pixel key definitions.

## Pixel Keys

Each pixel type is represented by a unique pixel key defined in the YAML frontmatter.

### Best Practices

Pixel Key Formats:
  - Single-digit hex (0-F): For files with up to 16 colors.
  - Two-digit hex (00-FF): For files with up to 256 colors.

## Pixel Mapping

- Whitespace: Only spaces or tabs are allowed as separators between pixel keys in the pixel mapping section.
- Dimensions:
  - Width: Determined by the number of pixel keys in the longest row.
  - Height: Determined by the number of pixel mapping rows.
- Comments: Lines beginning with `#` are treated as comments and ignored during parsing.

### Best Practices

- Uniformity: All pixel mapping rows should contain the same number of pixel keys.
