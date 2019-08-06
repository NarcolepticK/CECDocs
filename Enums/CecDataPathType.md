# CecDataPathType

    CEC_PATH_MBOX_LIST = 1,    /// data:/CEC/MBoxList____
    CEC_PATH_MBOX_INFO = 2,    /// data:/CEC/<id>/MBoxInfo____
    CEC_PATH_INBOX_INFO = 3,   /// data:/CEC/<id>/InBox___/BoxInfo_____
    CEC_PATH_OUTBOX_INFO = 4,  /// data:/CEC/<id>/OutBox__/BoxInfo_____
    CEC_PATH_OUTBOX_INDEX = 5, /// data:/CEC/<id>/OutBox__/OBIndex_____
    CEC_PATH_INBOX_MSG = 6,    /// data:/CEC/<id>/InBox___/_<message_id>
    CEC_PATH_OUTBOX_MSG = 7,   /// data:/CEC/<id>/OutBox__/_<message_id>
    CEC_PATH_ROOT_DIR = 10,    /// data:/CEC
    CEC_PATH_MBOX_DIR = 11,    /// data:/CEC/<id>
    CEC_PATH_INBOX_DIR = 12,   /// data:/CEC/<id>/InBox___
    CEC_PATH_OUTBOX_DIR = 13,  /// data:/CEC/<id>/OutBox__
    CEC_MBOX_DATA = 100,       /// data:/CEC/<id>/MBoxData.0<i-100>
    CEC_MBOX_ICON = 101,       /// data:/CEC/<id>/MBoxData.001
    CEC_MBOX_TITLE = 110,      /// data:/CEC/<id>/MBoxData.010
    CEC_MBOX_PROGRAM_ID = 150  /// data:/CEC/<id>/MBoxData.050
