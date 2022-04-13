Research: CoDec

**CoDec:**
The main factors that we’re gonna look to judge a CoDec to be good or not are Compression rate, Compression and Decompression speeds.


- **Zlib (DEFLATE)**

**–**Zlib uses a combination of LZ77 and Huffman coding to compress data.

While the decompression algorithm is the inflate method, which takes a deflate bit stream for decompression and correctly produces the original full-size data or file.** 

**–**Compresses web pages and CSS files before sending them to the browser. And therefore drastically reduces transfer time since the files are much smaller.

**–**Zlib provides a good balance of speed and compression efficiency which makes it a widely used CoDec. 

**–**The Dictionary size used is 32 KB.

**–** Related links:

`      `<https://zlib.net/>

`      `<https://en.wikipedia.org/wiki/Zlib>

`      `<https://github.com/madler/zlib>

- **Deflate64 / Enhanced Deflate**

**–** Deflate64 is a proprietary variant of Deflate and uses the same algorithm.

**–** Used to compress web pages and CSS files before sending them to the browser. 

**–** Deflate64 takes longer compression time, But with a slightly higher compression ratio, than Deflate.

**–** Dictionary size is increased from 32 KB to 64 KB as compared to normal Deflate.

**–** Related links:

`	`<https://github.com/brianhelba/zipfile-deflate64>

`	`<https://en.wikipedia.org/wiki/Deflate#Deflate64/Enhanced_Deflate>

- **ZStandard (ZSTD)**

**–** A fast and lossless compression algorithm used for real-time compression at zlib-level which results in better compression ratios. zstd is much like the zip algorithm as it uses an LZ77-style dynamic dictionary followed by an entropy encoder.

**–** The Linux kernel has included Zstandard as a compression method for the btrfs and squashfs filesystems.

**–** Offers much faster compression and decompression and 2x faster speed and 12-15% smaller files as compared to HHVM binary and bytecode.

**–** Zstd package includes parallel (multi-threaded) implementations of both compression and decompression.

**–** Related links:

`	`<https://en.wikipedia.org/wiki/Zstd>

`	`<https://github.com/facebook/zstd>

`	`<https://facebook.github.io/zstd/>

- **Blosc**

**–** A compressor that uses the blocking technique to reduce activity on the memory bus as much as possible. In short, this blocking technique works by dividing datasets in blocks that are small enough to fit in the caches of modern processors and perform compression/decompression there.

**–** Blosc is meant to support all platforms where a C89 compliant C compiler can be found, such as Intel (Linux, Mac OSX and Windows) and ARM (Linux).

**–** Designed to transfer data to the processor cache faster than the traditional, non-compressed. Blosc compressor not only reduces the size of large datasets but also accelerates memory related computations.

**–** Capable of using multi threading capabilities of CPU, in order to make the compression and decompression process fast.

**–** Related links:

`	`<https://github.com/Blosc/c-blosc>

`	`<https://www.blosc.org/pages/blosc-in-depth/>

- **Brotli**

**–** Brotli is a generic-purpose lossless compression algorithm that compresses data using a combination of a modern variant of the LZ77 algorithm, Huffman coding and 2nd order context modeling.

**–** Primarily used to compress HTTP content in web servers and content delivery networks that results in making internet websites load faster.

**–** Supported and used by major web browsers due to better compression capabilities than gzip. It is similar in speed as compared to deflate but offers more dense compression.

**–** Compression efficiency.

JavaScript files compressed are roughly 15% smaller, CSS files are around 16% smaller and HTML files are around 20% smaller.

**–** Related links:

`	`<https://github.com/google/brotli>

`	`<https://en.wikipedia.org/wiki/Brotli>

- **Snappy**

**–** A compression format and program library introduced by Google and defined as a raw stream format, plus a higher-level "framing format" that can be used as a file format.

**–** Majorly used in compressing plain text, HTML, PNGs and JPEGs

**–** Compression efficiency.

Compression ratio of 1.5-1.7x for plain text, about 2-4x for HTML, and 1.0x for PNGs, JPEGs and other already-compressed data.

**–** The compression speeds are very fast which is achieved by losing on the compression ratios, Therefore the resulting output is 20-100% larger than that of other libraries.

`	`**–** Related links:

`		`<https://en.wikipedia.org/wiki/Snappy_(compression)>

`		`<https://github.com/google/snappy>

- **LZMA**

**–** LZMA, A lossless data compression algorithm that uses a dictionary compression algorithm (a variant of LZ77 with huge dictionary sizes and special support for repeatedly used match distances) using a complex model to make a probability prediction of each bit.

**–** Mainly used in Unix Operating system and kind of the same data compression algorithm as Zstd.

`	`**–** Compression is really high as compared to other algorithms.

`	`**–** Uses .lzma as file extension and variable dictionary size.

**–** Related links:

`	`[Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#:~:text=The%20Lempel%E2%80%93Ziv%E2%80%93Markov%20chain,of%20the%207%2DZip%20archiver.)

`	`[Github](https://github.com/chemfiles/lzma)


- **LZS**

**–** LZS uses a combination of fixed Huffman coding and sliding window compression algorithm. It uses the last 2 KB of uncompressed data as a sliding-window dictionary. An LZS compressor looks for matches between the data to be compressed and the last 2 KB of data. If it finds a match, it encodes an offset/length reference to the dictionary.

**–** It was originally developed for tape compression, and subsequently adapted for hard disk compression and later specified as a compression algorithm for various network protocols.

**–** Compression and decompression speeds are fairly good as compared to other CoDec.

**–** Dictionary size is variable and is similar to LZ77 CoDec.

**–** Related links:

`	`[Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Stac)

`	`[GitHub](https://github.com/m-boutaleb/LZS)


- **LZSS**

– A lossless data compression algorithm derived from LZ77, That uses a dictionary coding technique. It attempts to replace a string of symbols with a reference to a dictionary location of the same string.

– Apple's Mac OS X uses LZSS as one of the compression methods for kernel code.

– Many popular archivers like PKZip, ARJ, RAR, ZOO, LHarc use LZSS as the primary compression algorithm.

– Related links:

`	`[Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Storer%E2%80%93Szymanski)

`	`[GitHub](https://github.com/MichaelDipperstein/lzss)

- **BZ2**

– BZ2 or BZip2 is a free and open-source compression technique that uses Burrows–Wheeler algorithm and only compresses single files and not a file archiver.

– Mostly used in big data applications with cluster computing frameworks like Hadoop and Apache Spark.

– More effective than the older LZW and Deflate compression algorithms, but is considerably slower. LZMA is generally more space-efficient than bzip2 at the expense of even slower compression speed, while having much faster decompression.

– Compression ratio varies between 10% to 15% as compared to the best CoDec algorithm.

– Related links:

`	`[Wikipedia](https://en.wikipedia.org/wiki/Bzip2)

`	`[Python-BZ2](https://docs.python.org/3/library/bz2.html)

`	`[GitHub](https://github.com/libarchive/bzip2)

- **LZ4,** 

**–** The LZ4 algorithm works by representing the data as a series of sequences. Each sequence begins with a one-byte token that is broken into two 4-bit fields. The first field represents the number of literal bytes that are to be copied to the output.

– This algorithm provides a good combination of speed and compression. But not very useful in the latest test cases.

– Provides a smaller or we can say worse compression ratio than LZO algorithm, and even more worse when compared to DEFLATE.

– Uses .lz4 as file extension.

– Related links:

`	`[GitHub](https://github.com/lz4/lz4)
`	`[Wikipedia](https://en.wikipedia.org/wiki/LZ4_\(compression_algorithm\))

- **LZ4HC,** 

– LZ4HC is a "high-compression" variant of LZ4 in which the compressor finds more than one match between current and past data and looks for the best match to ensure the output is small.

– The Apache Hadoop system uses this algorithm for fast compression. LZ4 was also implemented natively in the Linux kernel.

–  LZ4HC has a high compression ratio but low compression speed as compared to LZ4.

– LZ4HC compression makes it possible to load individual Assets from an Asset Bundle quickly and using less memory than LZMA compressed Asset Bundles.

– Related LInks:

`	`[Github](https://github.com/bwlewis/lz4/blob/master/src/lz4hc.h)
`	`[Doc](https://hg.mozilla.org/mozilla-central/file/tip/mfbt/lz4/lz4hc.h)

- **LZW,** 

– LZW compression uses a table-based lookup algorithm that identifies repeated sequences in the data and adds them to the code table. Also the Decoding is achieved by taking each code from the compressed file and translating it through the code table to find what character or characters it represents.

– Most commonly used to compress GIF image format served from Web sites and the TIFF image format.

– The advantage of LZW is its simplicity, fast execution.
– Related Links:

`	`[Doc](https://www.geeksforgeeks.org/lzw-lempel-ziv-welch-compression-technique/)
`	`[Github](https://github.com/MichaelDipperstein/lzw)

- **LZX**

– LZX is a LZ77 family compression algorithm. Like LZ77, It’s also a dictionary codec and uses a sliding window during compression.
– Mainly used in Amiga LZX, Microsoft Cabinet files, Microsoft Compressed HTML Help (CHM) files, Microsoft Reader (LIT) files, CompactOS NTFS file compression etc.
– As LZX is used widely, the compression and decompression speed may vary as per its Instances of use.
– Related Links:
`	`[Wikipedia](https://en.wikipedia.org/wiki/LZX)


- **LZWL**

**–** LZWL is a syllable-based variant of the character-based LZW compression algorithm and works over the alphabet of syllables therefore this algorithm can be used with words also.

– Being a variant of LZW compression, uses are also the same.
– Compression speeds are fast and even more fast in selective cases.
– Related Links:
`	`[Wikipedia](https://en.wikipedia.org/wiki/LZWL)


- **LZF,** 

– A Java library with no Huffman-encoding is used for encoding and decoding data in LZF format.

– This algorithm is optimized for speed with an average compression ratio.

– When compared to standard Deflate algo LZF can give 5 to 6 times faster compression and 2 times faster decompression.

– Compression rate is lower since no Huffman-encoding is used.

- **LZO**

**–** LZO is a block compression algorithm as it compresses and decompresses blocks of data. Block size must be the same for compression and decompression. LZO compresses a block of data into matches (a sliding dictionary) and runs of non-matching literals to produce good results on highly redundant data

– Higher compression and decompression speeds as compared to DEFLATE compression.

– Requires an additional buffer during compression (of size 8 kB or 64 kB, depending on compression level)

– Allows the user to adjust the balance between compression ratio and compression speed, without affecting the speed of decompression.

– Related Links:
`	`[Github](https://github.com/nemequ/lzo)
`	`[Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Oberhumer)
`	`[Website](http://www.oberhumer.com/opensource/lzo/)

- **LZFSE
  –** LZFSE (Lempel–Ziv Finite State Entropy) is an open source lossless data compression algorithm created by Apple Inc. It was released with a simpler algorithm called LZVN.[2]

– LZFSE is used for compressing a payload for iOS, macOS, watchOS, and tvOS.

– LZFSE compresses with a ratio comparable to that of zlib (DEFLATE) and decompresses two to three times faster while using fewer resources, therefore offering higher energy efficiency than zlib.

–  LZFSE is similar in speed to ZSTD (level 6), but has a slightly worse ratio.
– Related Links:
`	`[Wikipedia](https://en.wikipedia.org/wiki/LZFSE)
`	`[GitHub](https://github.com/lzfse/lzfse)

- **LZJB**

– LZJB is a lossless data compression algorithm to compress crash dumps and data in ZFS. Basically it is the improved version of LZRW1 algorithm

– **Pending** due to Less info available.
– Related links:
`	`[Wikipedia](https://en.wikipedia.org/wiki/LZJB)

- **LZRW**

– LZRW(Lempel–Ziv Ross Williams) refers to variants of the LZ77 lossless data compression algorithms with an emphasis on improving compression speed through the use of hash tables and other techniques.
– There are many variants of LZRW i.e

LZRW1[2], LZRW1-A, LZRW2, LZRW3, LZRW3-A, LZRW4, LZRW5
– Both the LZRW1-A and LZRW3 use the same hash table lookups to identify matches, and so provide (almost) identical compression. However, LZRW1 transmits the match information as offset/length pairs, whereas LZRW3 transmits hash/length pairs, allowing greater history depths to be referenced at the expense of maintaining an identical hash table at the decompressor.
– Related links:
`	`[Comparison](https://www.heliontech.com/comp_info.htm)
`	`[Wikipedia](https://en.wikipedia.org/wiki/LZRW)

- **ZFP**
  – zfp was designed to achieve high compression ratios and therefore uses lossy but optionally error-bounded compression. Bit-for-bit lossless compression of integer and floating-point arrays is also supported.
  – zfp is a compressed format for representing multidimensional floating-point and integer arrays. zfp provides compressed-array classes that support high throughput read and write random access to individual array elements. zfp also supports serial and parallel (OpenMP and CUDA) compression of whole arrays.
  – zfp is often more accurate and faster than other lossy compressors, especially in its OpenMP and CUDA multithreaded modes.

– zfp is designed to achieve high compression ratios and also works best for 2D, 3D, and 4D arrays that exhibit spatial correlation, such as continuous fields from physics simulations, natural images, regularly sampled terrain surfaces, etc.
– Related links:
`	`[GitHub](https://github.com/LLNL/zfp)
`	`[Official page](https://computing.llnl.gov/projects/zfp)

- **AEC**
  – Acoustic Echo Cancellation (AEC) is used to efficiently process the microphone audio so that audio coming from the loudspeaker is removed from the microphone signal.

– Acoustic echo cancellation (AEC) technology is a common addition to today's conference phones. The technology recognizes and eliminates the echo as quickly as possible without affecting the audio quality.
– Related links:
`	`[Wikipedia](https://en.wikipedia.org/wiki/Echo_suppression_and_cancellation)
`	`[Link](https://wiki.analog.com/resources/tools-software/sigmastudio/toolbox/adialgorithms/aec) 

- **LERC**
  LERC is an open-source image or raster format which supports rapid encoding and decoding for any pixel type (not just RGB or Byte). Users set the maximum compression error per pixel while encoding, so the precision of the original input image is preserved (within user defined error bounds).

- **NPY**
  ` `the standard binary file format in NumPy for persisting a single arbitrary NumPy array on disk. The format stores all of the shape and dtype information necessary to reconstruct the array correctly even on another machine with a different architecture.

npz file format is a zipped archive of files named after the variables they contain. The archive is not compressed and each file in the archive contains one variable in npz file with load a NpzFile object is returned. This is a dictionary-like object which can be queried for its list of arrays (with the .

- **APNG**
  Animated Portable Network Graphics (APNG) is a file format which extends the Portable Network Graphics (PNG) specification to permit animated images that work similarly to animated GIF files, while supporting 24-bit images and 8-bit transparency not available for GIFs. It also retains backward compatibility with non-animated PNG files.

–Apng is a better format. GIF and apng are both lossless, but apng tend to be smaller, and better quality (more colors, and the ability for transparency) Unfortunately apng are largely unsupported, but that may change.

- **PNG**

Portable Network Graphics (PNG) is a raster-graphics file format that supports lossless data compression.
–Both PNG and TIFF files benefit from lossless compression, meaning that no matter how often you save, open, or resize them, they'll maintain their quality. However, TIFF files offer users a choice between lossy and lossless compression, which can help reduce the file size if this is a priority.

–The biggest advantage of PNG over JPEG is that the compression is lossless, meaning there is no loss in quality each time it is opened and saved again.

- **GIF**
  On modern hardware GIF is the slowest and most expensive video codec.
  –The format supports up to 8 bits per pixel for each image, allowing a single image to reference its own palette of up to 256 different colors chosen from the 24-bit RGB color space. It also supports animations and allows a separate palette of up to 256 colors for each frame. These palette limitations make GIF less suitable for reproducing color photographs and other images with color gradients, but well-suited for simpler images such as graphics or logos with solid areas of color.

– GIF images are compressed using the Lempel–Ziv–Welch (LZW) lossless data compression technique to reduce the file size without degrading the visual quality.

- **TIFF**
  A TIFF, which stands for Tag Image File Format, is a computer file used to store raster graphics and image information. A favorite among photographers, TIFFs are a handy way to store high-quality images before editing if you want to avoid lossy file formats.

– TIFF is uncompressed. Since TIFF does not use any compression algorithms like JPEG or GIF formats, the file contains more data and results in a more detailed picture. However, because TIFF files contain more data, the files are large and take up a lot of storage space.

- **WebP**
  WebP is a modern image format that provides lossless and lossy compression for smaller, richer images on the web. Play specified types of media with this extension for Windows 10.
  – WebP is an image file format that Google has developed as a replacement for JPEG, PNG, and GIF file formats. WebP yields files that are smaller for the same quality, or of higher quality for the same size.[6] It supports both lossy and lossless compression,[7] as well as animation and alpha transparency.

The following CoDec are kind of similar ones….

- **JPEG 8-bit**
  JPEG (/ˈdʒeɪpɛɡ/ JAY-peg)[2] is a commonly used method of lossy compression for digital images, particularly for those images produced by digital photography. The degree of compression can be adjusted, allowing a selectable tradeoff between storage size and image quality. JPEG typically achieves 10:1 compression with little perceptible loss in image quality.[3]

–  JPEG/JFIF supports a maximum image size of 65,535×65,535 pixels,[10] hence up to 4 gigapixels for an aspect ratio of 1:1. In 2000, the JPEG group introduced a format intended to be a successor, JPEG 2000, but it was unable to replace the original JPEG as the dominant image standard.[11]

– "JPEG" stands for Joint Photographic Experts Group,

– The JPEG compression algorithm operates at its best on photographs and paintings of realistic scenes with smooth variations of tone and color. For web usage, where reducing the amount of data used for an image is important for responsive presentation, JPEG's compression benefits make JPEG popular. JPEG/Exif is also the most common format saved by digital cameras.

However, JPEG is not well suited for line drawings and other textual or iconic graphics, where the sharp contrasts between adjacent pixels can cause noticeable artifacts. Such images are better saved in a lossless graphics format such as TIFF, GIF, PNG, or a raw image format. The JPEG standard includes a lossless coding mode, but that mode is not supported in most products.

As the typical use of JPEG is a lossy compression method, which reduces the image fidelity, it is inappropriate for exact reproduction of imaging data (such as some scientific and medical imaging applications and certain technical image processing work).

- **JPEG 12-bit,** 

The new version of the ‘libjpeg’ library, as it’s called, is making headlines because, not only does it support 12-bit color depth and additional scaling functions, the new standard also supports more compression options including completely lossless compression.

– So, while it might be some time still before any photographic hardware or software adopts the standard, this ability could potentially make it a competitor for both RAW and TIFF files when it comes to working with and archiving photographs.

- **Lossless JPEG (LJPEG, SOF3), 
  –** ossless JPEG was developed as a late addition to JPEG in 1993, using a completely different technique from the lossy JPEG standard. It uses a predictive scheme based on the three nearest (causal) neighbors (upper, left, and upper-left), and entropy coding is used on the prediction error. The standard Independent JPEG Group libraries cannot encode or decode it, but Ken Murchison of Oceana Matrix Ltd. wrote a patch that extends the IJG library to handle lossless JPEG.[1] Lossless JPEG has some popularity in medical imaging, and is used in DNG and some digital cameras to compress raw images, but otherwise was never widely adopted. Adobe's DNG SDK provides a software library for encoding and decoding lossless JPEG with up to 16 bits per sample.

- **JPEG 2000,**

**–**JPEG 2000 (JP2) is an image compression standard and coding system. It was developed from 1997 to 2000 by a Joint Photographic Experts Group committee chaired by Touradj Ebrahimi (later the JPEG president),[1] with the intention of superseding their original discrete cosine transform (DCT) based JPEG standard (created in 1992) with a newly designed, wavelet-based method. The standardized filename extension is .jp2 for ISO/IEC 15444-1 conforming files and .jpx for the extended part-2 specifications, published as ISO/IEC 15444-2. The registered MIME types are defined in RFC 3745. For ISO/IEC 15444-1 it is image/jp2.

JPEG 2000 code streams are regions of interest that offer several mechanisms to support spatial random access or region of interest access at varying degrees of granularity. It is possible to store different parts of the same picture using different quality.

JPEG 2000 is a discrete wavelet transform (DWT) based compression standard that could be adapted for motion imaging video compression with the Motion JPEG 2000 extension. JPEG 2000 technology was selected as the video coding standard for digital cinema in 2004.[2]

- **JPEG LS,** 

JPEG-LS is a lossless/near-lossless compression standard for continuous-tone images. Its official designation is ISO-14495-1/ITU-T. 87. It is a simple and efficient baseline algorithm which consists of two independent and distinct stages called modeling and encoding.

– PEG-LS was developed with the aim of providing a low-complexity lossless and near-lossless image compression standard that could offer better compression efficiency than lossless JPEG. It was developed because at the time, the Huffman coding-based JPEG lossless standard and other standards were limited in their compression performance

– 

- **JPEG XR (WDP, HD Photo),** 
  The JPEG XR standard provides a practical coding technology for a broad range of applications with excellent compression capability and important additional functionalities. The primary intended application of JPEG XR is the representation of continuous-tone still images such as photographic images.

As of 2008, the most widely used digital photography format is a nominal implementation of the first JPEG coding format as specified in Rec. ITU-T T.81 | ISO/IEC 10918-1. This encoding uses a bit depth of 8 for each of three channels, resulting in 256 representable values per channel (a total of 16 777 216 representable color values). More demanding applications may require a bit depth of 16, providing 65,536 representable values for each channel, and resulting in over 2.8 \* 10^14 color values. Additional scenarios may necessitate even greater bit depths and sample representation formats. When memory or processing power is at a premium, as few as five or six bits per channel may be used.

The JPEG XR specification enables greater effective use of compressed imagery with this broadened diversity of application requirements. JPEG XR supports a wide range of color encoding formats including monochrome, RGB, CMYK and n-component encodings using a variety of unsigned integer, fixed point, and floating point decoded numerical representations with a variety of bit depths. The primary goal is to provide a compressed format specification appropriate for a wide range of applications while keeping the implementation requirements for encoders and decoders simple. A special focus of the design is support for emerging high dynamic range (HDR) imagery applications.
**



- **JPEG XL,** 
  JPEG XL includes a lossless/near-lossless/responsive mode called Modular which optionally uses a modified Haar transform (called "squeeze") and which is also used to encode the DC (1:8 scale) image in VarDCT mode as well as various auxiliary images such as adaptive quantization fields or additional channels like alpha.[15]

- **JPEG XT,**
  JPEG XT includes a lossless integer-to-integer DCT transform mode based on wavelet compression from JPEG 2000.

- **MOZJPEG
  –** Today I'd like to announce a new Mozilla project called 'mozjpeg'. The goal is to provide a production-quality JPEG encoder that improves compression while maintaining compatibility with the vast majority of deployed decoders. ... It's the most popular lossy compressed image format on the Web, and has been for a long time.
  – MozJPEG supports both Lossy & Lossless compression. It comes with two executables/binaries, cjpeg & jpegtran.

- **AVIF
  –** AVIF is lossless which means that the file size is compressed, but the picture quality still remains the same. However, doing some test comparisons the AVIF lossless mode isn't very good. WebP and even PNG outperformed the lossless AVIF image in byte sizes.

– Like VP9, but unlike H. 264/AVC and HEVC, AV1 has a royalty-free licensing model that does not hinder adoption in open-source projects. AVIF is an image file format that uses AV1 compression algorithms.

- **PackBits**
  PackBits is a fast, simple lossless compression scheme for run-length encoding of data

– To Do…..

- **Delta**
  Delta encoding is a way of storing or transmitting data in the form of differences (deltas) between sequential data rather than complete files; more generally this is known as data differencing. Delta encoding is sometimes called delta compression, particularly where archival histories of changes are required (e.g., in revision control software).





**–  Difference: LZ77 vs. LZ4 vs. LZ4HC (compression algorithms)?**

LZ4 is built to compress fast, at hundreds of MB/s per core. It's a fit for applications where you want compression that's very cheap: for example, you're trying to make a network or on-disk format more compact but can't afford to spend a bunch of CPU time on compression. It's in a family with, for example, snappy and LZO.

The natural comparison point is zlib's DEFLATE algorithm, which uses LZ77 and Huffman coding and is used in gzip, the .ZIP and .PNG formats, and too many other places to count.

These fast compressors differ because:

They use repetition-detection code that's faster (often a simple hashtable with no collision detection) but doesn't search through multiple possible matches for the best one (which would take time but result in higher compression), and can't find some short matches.

They only try to compress repetitions in input--they don't try to take advantage of some bytes being more likely than others outside of repetitions.

Closely related to 2, they generate bytes of output at a time, not bits; allowing fraction-of-a-byte codes would allow for more compression sometimes, but would require more CPU work (often bit-shifting and masking and branching) to encode and decode.

Lots of practical work has gone into making their implementations fast on modern CPUs.

By comparison, DEFLATE gets better compression but compresses and decompresses slower, and high-compression algorithms like LZMA, bzip2, LZHAM, or brotli tend to take even more time (though Brotli at its faster settings can compete with zlib). There's a lot of variation among the high-compression algorithms, but broadly, they tend to capture redundancies over longer distances, take more advantage of context to determine what bytes are likely, and use more compact but slower ways to express their results in bits.

LZ4HC is a "high-compression" variant of LZ4 that, I believe, changes point 1 above--the compressor finds more than one match between current and past data and looks for the best match to ensure the output is small. This improves compression ratio but lowers compression speed compared to LZ4. Decompression speed isn't hurt, though, so if you compress once and decompress many times and mostly want extremely cheap decompression, LZ4HC would make sense.

Note that even a fast compressor might not allow one core to saturate a large amount of bandwidth, like that provided by SSDs or fast in-datacenter links. There are even quicker compressors with lower ratios, sometimes used to temporarily pack data in RAM. WKdm and Density are two such compressors; one trait they share is acting on 4-byte machine words of input at a time rather than individual bytes. Sometimes specialized hardware can achieve very fast compression, like in Samsung's Exynos chips or Intel's QuickAssist technology.

If you're interested in compressing more than LZ4 but with less CPU time than deflate, the author of LZ4 (Yann Collet) wrote a library called Zstd--here's a blog post from Facebook at its stable release, background on the finite state machines used for compactly encoding info on repetitions, and a detailed description in an RFC. Its fast modes could work in some LZ4-ish use cases. (Also, Apple developed lzfse on similar principles, and Google developed gipfeli as a 'medium' packer. Neither seemed to get much use in the outside world.) Also, a couple projects aim to provide faster/lighter DEFLATE: SLZ and patches to zlib by CloudFlare and Intel.

Compared to the fastest compressors, those "medium" packers add a form of entropy encoding, which is to say they take advantage of how some bytes are more common than others and (in effect) put fewer bits in the output for the more common byte values.

If you're compressing one long stream, and going faster using more cores is potentially helpful, parallel compression is available for gzip through pigz and the zstd through the command-line tool's -T option (and in the library). (There are various experimental packers out there too, but they exist more to push boundaries on speed or density, rather than for use today.)

So, in general, you have a pretty good spectrum of alternative compressors for different apps:

For very fast compression: LZ4, zstd's lowest settings, or even weaker memory compressors

For balanced compression: DEFLATE is the old standard; Zstd and brotli on low-to-medium settings are good alternatives for new uses

For high compression: brotli, or Zstd on high settings

For very high compression (like static content that's compressed once and served many times): brotli

As you move from LZ4 through DEFLATE to brotli you layer on more effort to predict and encode data and get more compression out at the cost of some speed.

As an aside, algorithms like brotli and zstd can generally outperform gzip--compress better at a given speed, or get the same compression faster--but this isn't actually because zlib did anything wrong. The main secret is probably that newer algos can use more memory: zlib dates to 1995 (and DEFLATE to 1993). Back then RAM cost >3,000x as much as today, so just keeping 32KB of history made sense. Changes in CPUs over time may also be a factor: tons of of arithmetic (as used in finite state machines) is relatively cheaper than it used to be, and unpredictable ifs (branches) are relatively more expensive.




The main difference between LZ77 and LZSS is that in LZ77 the dictionary reference could actually be longer than the string it was replacing. In LZSS, such references are omitted if the length is less than the "break even" point. Furthermore, LZSS uses one-bit flags to indicate whether the next chunk of data is a literal (byte) or a reference to an offset/length pair.

- **LZ77 and LZ78**

LZ77 and LZ78 are the two lossless data compression algorithms published in papers by Abraham Lempel and Jacob Ziv in 1977[1] and 1978.[2] They are also known as LZ1 and LZ2 respectively.[3] These two algorithms form the basis for many variations including LZW, LZSS, LZMA and others. Besides their academic influence, these algorithms formed the basis of several ubiquitous compression schemes, including GIF and the DEFLATE algorithm used in PNG and ZIP.

They are both theoretically dictionary coders. LZ77 maintains a sliding window during compression. This was later shown to be equivalent to the explicit dictionary constructed by LZ78—however, they are only equivalent when the entire data is intended to be decompressed.

Since LZ77 encodes and decodes from a sliding window over previously seen characters, decompression must always start at the beginning of the input. Conceptually, LZ78 decompression could allow random access to the input if the entire dictionary were known in advance. However, in practice the dictionary is created during encoding and decoding by creating a new phrase whenever a token is output.[4]








Pending

- **Packed** 
- **Integers,** 
- **LZ4F**
- **XOR Delta,** 
- **Floating Point Predictor**
- **Bitorder reversal,** 
- **Bitshuffle, CMS (color space transformations)**
- **Float24 (24-bit floating point)**
- **PGLZ (PostgreSQL LZ)**
  – To Do…

- **RCOMP (Rice)**
  – To Do….
