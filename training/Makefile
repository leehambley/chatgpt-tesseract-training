# Define variables
LANG_ID=datsun-microfilm
TESSDATA_PREFIX=/usr/share/tesseract-ocr/4.00/tessdata/
TRAINING_IMAGE=cropped_parts_table.$(LANG_ID).training.tiff
BOX_FILE=cropped_parts_table.$(LANG_ID).training.box
FONT_PROPERTIES=font_properties
OUTPUT_DIR=.

# all: train

# train: generate_tr_files mftraining cntraining rename_files combine_tessdata copy_traineddata

# generate_tr_files:
# 	tesseract $(TRAINING_IMAGE) $(OUTPUT_DIR)/$(LANG_ID).training box.train

# mftraining:
# 	mftraining -F $(FONT_PROPERTIES) -U unicharset -O $(OUTPUT_DIR)/$(LANG_ID).unicharset $(OUTPUT_DIR)/$(LANG_ID).training.tr

# cntraining:
# 	cntraining $(OUTPUT_DIR)/$(LANG_ID).training.tr

# rename_files:
# 	mv inttemp $(OUTPUT_DIR)/$(LANG_ID).inttemp
# 	mv normproto $(OUTPUT_DIR)/$(LANG_ID).normproto
# 	mv pffmtable $(OUTPUT_DIR)/$(LANG_ID).pffmtable
# 	mv shapetable $(OUTPUT_DIR)/$(LANG_ID).shapetable

# combine_tessdata:
# 	combine_tessdata $(OUTPUT_DIR)/$(LANG_ID).

# copy_traineddata:
# 	sudo cp $(OUTPUT_DIR)/$(LANG_ID).traineddata $(TESSDATA_PREFIX)

create_tr_file:
	tesseract $(TRAINING_IMAGE) $(OUTPUT_DIR)/$(LANG_ID).training box.train

.PHONY: all create_tr_file
