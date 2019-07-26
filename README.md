# SRA submission

## Glossary

<b>Sequence Read Archive (SRA) number</b>: A Sequence Read Archive (SRA) number of the format SRP123456 is generated by the SRA database on submission of sequencing data. <b>Most journals require this number to be included in the manuscript</b>. 

<b>BioProject</b>: A BioProject should be created for every SRA submission. A BioProject ID is of the format PRJNA12345 and is synonymous with an SRA number. Once a BioProject is registered, the submitter receives an email with a link to access the project information once the data has been released. Some journals require this link to be included in the manuscript. 

<b>BioSample</b>: Multiple BioSamples can be part of one BioProject. Usually, every replicate in the screening data is entered as one BioSample. A single BioSample can have multiple fastq files associated with it. For example, if a sample has been sequenced using the Illumina NextSeq platform, this sample will have 4 lanes of sequencing associated with it, i.e. 4 fastq files. All 4 fastq files can be uploaded as part of one BioSample. 


To submit screening data to SRA, first create an account with NCBI if you do not already have one. Then, create a new “BioProject” here for your submission. The steps to do this are as follows:
<ol>
  <li>Click on the “New Submission” button and fill in all the required submitter information. </li>
  <li>To submit sequencing data for a standard CRISPR screen sequenced by GPP, the “Project data type” should be  “Raw sequence reads”. The sample scope should then be selected appropriately from the drop-down menu. </li>
  <li>The following page is populated based on the selected scope. Enter information here about the sample organism. 
Continue to then select when the data should be released, include a “Project Title” (usually the title of the manuscript) and a description about the project (usually the abstract of the manuscript). You can also include grants and consortia associated with the project in this page. </li>
    <li>If you are submitting more than on one BioSample complete the BioProject without entering a BioSample number. The BioSamples can be created later using the BioProject number of the format PRJNA# you receive.</li>
</ol>
To submit your BioSamples, first click the “New Submission” button here and fill in all the required submitter information. Then:
<ol>
  <li>Select when the data should be released and then select “Batch/Multiple BioSamples”. </li>
  <li>Next, select the BioSample “package” that fits your data best. If all samples are human cell lines, select “Human sample”.</li>
  <li>BioSample attributes can then be filled in using the “built-in table editor” or by downloading a file in Excel/TSV format and uploading the filled-in file. Using the file is the preferred option as the webpage with the built-in table editor times out and all the data in the table has to be re-entered for every login.</li>
  <li>BioSample metadata should be filled in appropriately and uploaded. Each BioSample should be included as a separate row in this file. A few points to remember while entering information: </li>
  <ol>
    <li type='a'>Carefully fill in the information. After submitting the BioSamples, changes can only be made by emailing NCBI. </li>
    <li type='a'>More columns of information can be appended to make the sample information more distinct. An error is generated during the processing of this file if majority of the columns for 2 or more samples are similar. </li>
    <li type='a'>Make sure to include the right BioProject accession in the “bioproject_accession” column if you have already submitted a BioProject. </li>
    <li type='a'>In the Excel format of the file, hovering over the column names helps understanding what value should be entered in the column.</li> 
  </ol>
  <li>Once the file has been filled in as per the requirement, uploaded and processed, BioSample submission is complete. The submitter then receives an email with accession numbers of the form SAMN12345678 for all the submitted BioSamples. This email also includes links to access each BioSample after release of the data. </li>
  <li>Multiple batch BioSample submissions can be associated with a single BioProject. The appropriate BioProject accession should be entered in the attributes file. </li>
  <ol><li type='a'>If all fastq files for data included in the paper are not ready for submission, a few files can be uploaded to receive an SRA number to be included in the manuscript. Remaining fastq files can be uploaded later by including the same BioProject accession in the attributes file of the BioSamples. In the BioSample attributes file only include information about the BioSamples for which fastq files are ready for submission. </li></ol>
</ol>
Once a BioProject has been created and the BioSamples have been submitted, start a new SRA submission here by clicking on “New Submission” and fill in all the required submitter information. 
<ol>
  <li>If you have already submitted a BioProject, enter the BioProject accession of the form PRJNA12345. Then, select “Yes” if BioSamples have been submitted and select when the data should be released. </li>
  <li>Next, fill in the SRA metadata by using the built-in editor or by downloading the file in Excel/TSV format. Downloading the file is the preferred option. Points to remember when filling this table:</li>
  <ol>
    <li type='a'>Enter the appropriate BioProject accession of the form PRJNA# and BioSample accessions of the form SAMN#. If the built-in editor is used, the BioProject accession and BioSample accessions can be selected from a pre-populated drop-down menu. </li>
    <li type='a'>The library_ID can be similar to the Sample Name entered in the BioSample attributes file. Each library_ID should be unique. </li>
    <li type='a'>Information about sequencing such as the platform, instrument model, and library layout can be obtained from GPP.</li>
    <li type='a'>Make sure the fastq file names entered for each BioSample matches with the names of the fastq files to be uploaded. </li>
    <li type='a'>Multiple fastq files can be uploaded for a single BioSample. </li>
    <li type='a'>All the files you intend to upload should be included in the SRA metadata file. </li>
  </ol>
  <li>Once the SRA metadata file has been filled and uploaded, this portal can be used to upload files. The following page gives 3 options for file upload. The “Web browser upload via HTTP or Aspera Connect plugin” option should only be used if only few files need to be uploaded. The page provides detailed instructions regarding file upload using the FTP or Amazon S3 bucket. </li>
  <li>Files should be uploaded after which SRA submission is complete. </li>
</ol>

<p><b>Preparing sequence files for SRA/GEO submission</b></p>

<b>Demultiplexing of FASTQ files</b>: All sequencing files submitted should be of FASTQ format as received from the sequencing instrument. SRA/GEO require that the fastq files be demultiplexed such that each barcoded sample ends up with at least one dedicated run file. Demultiplexed files can be obtained from GPP by request. Details required for demultiplexing files are:
<ol>
  <li type='a'>File with sample barcodes and sample conditions used in the manuscript.</li>
  <li type='a'>Sequencing ID or PoolQ ID or date of sequencing deconvolution to help locate sequencing files.</li>



