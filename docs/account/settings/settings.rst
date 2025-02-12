``a.settings``: Personal Compute Enablement
===========================================
.. currentmodule:: databricks.sdk.service.settings

.. py:class:: AccountSettingsAPI

    The Personal Compute enablement setting lets you control which users can use the Personal Compute default
    policy to create compute resources. By default all users in all workspaces have access (ON), but you can
    change the setting to instead let individual workspaces configure access control (DELEGATE).
    
    There is only one instance of this setting per account. Since this setting has a default value, this
    setting is present on all accounts even though it's never set on a given account. Deletion reverts the
    value of the setting back to the default value.

    .. py:method:: delete_personal_compute_setting( [, etag: Optional[str]]) -> DeletePersonalComputeSettingResponse

        Delete Personal Compute setting.
        
        Reverts back the Personal Compute setting value to default (ON)
        
        :param etag: str (optional)
          etag used for versioning. The response is at least as fresh as the eTag provided. This is used for
          optimistic concurrency control as a way to help prevent simultaneous writes of a setting overwriting
          each other. It is strongly suggested that systems make use of the etag in the read -> delete pattern
          to perform setting deletions in order to avoid race conditions. That is, get an etag from a GET
          request, and pass it with the DELETE request to identify the rule set version you are deleting.
        
        :returns: :class:`DeletePersonalComputeSettingResponse`
        

    .. py:method:: get_csp_enablement_account_setting( [, etag: Optional[str]]) -> CspEnablementAccountSetting

        Get the compliance security profile setting for new workspaces.
        
        Gets the compliance security profile setting for new workspaces.
        
        :param etag: str (optional)
          etag used for versioning. The response is at least as fresh as the eTag provided. This is used for
          optimistic concurrency control as a way to help prevent simultaneous writes of a setting overwriting
          each other. It is strongly suggested that systems make use of the etag in the read -> delete pattern
          to perform setting deletions in order to avoid race conditions. That is, get an etag from a GET
          request, and pass it with the DELETE request to identify the rule set version you are deleting.
        
        :returns: :class:`CspEnablementAccountSetting`
        

    .. py:method:: get_esm_enablement_account_setting( [, etag: Optional[str]]) -> EsmEnablementAccountSetting

        Get the enhanced security monitoring setting for new workspaces.
        
        Gets the enhanced security monitoring setting for new workspaces.
        
        :param etag: str (optional)
          etag used for versioning. The response is at least as fresh as the eTag provided. This is used for
          optimistic concurrency control as a way to help prevent simultaneous writes of a setting overwriting
          each other. It is strongly suggested that systems make use of the etag in the read -> delete pattern
          to perform setting deletions in order to avoid race conditions. That is, get an etag from a GET
          request, and pass it with the DELETE request to identify the rule set version you are deleting.
        
        :returns: :class:`EsmEnablementAccountSetting`
        

    .. py:method:: get_personal_compute_setting( [, etag: Optional[str]]) -> PersonalComputeSetting

        Get Personal Compute setting.
        
        Gets the value of the Personal Compute setting.
        
        :param etag: str (optional)
          etag used for versioning. The response is at least as fresh as the eTag provided. This is used for
          optimistic concurrency control as a way to help prevent simultaneous writes of a setting overwriting
          each other. It is strongly suggested that systems make use of the etag in the read -> delete pattern
          to perform setting deletions in order to avoid race conditions. That is, get an etag from a GET
          request, and pass it with the DELETE request to identify the rule set version you are deleting.
        
        :returns: :class:`PersonalComputeSetting`
        

    .. py:method:: update_csp_enablement_account_setting(allow_missing: bool, setting: CspEnablementAccountSetting, field_mask: str) -> CspEnablementAccountSetting

        Update the compliance security profile setting for new workspaces.
        
        Updates the value of the compliance security profile setting for new workspaces.
        
        :param allow_missing: bool
          This should always be set to true for Settings API. Added for AIP compliance.
        :param setting: :class:`CspEnablementAccountSetting`
        :param field_mask: str
          Field mask is required to be passed into the PATCH request. Field mask specifies which fields of the
          setting payload will be updated. The field mask needs to be supplied as single string. To specify
          multiple fields in the field mask, use comma as the separator (no space).
        
        :returns: :class:`CspEnablementAccountSetting`
        

    .. py:method:: update_esm_enablement_account_setting(allow_missing: bool, setting: EsmEnablementAccountSetting, field_mask: str) -> EsmEnablementAccountSetting

        Update the enhanced security monitoring setting for new workspaces.
        
        Updates the value of the enhanced security monitoring setting for new workspaces.
        
        :param allow_missing: bool
          This should always be set to true for Settings API. Added for AIP compliance.
        :param setting: :class:`EsmEnablementAccountSetting`
        :param field_mask: str
          Field mask is required to be passed into the PATCH request. Field mask specifies which fields of the
          setting payload will be updated. The field mask needs to be supplied as single string. To specify
          multiple fields in the field mask, use comma as the separator (no space).
        
        :returns: :class:`EsmEnablementAccountSetting`
        

    .. py:method:: update_personal_compute_setting(allow_missing: bool, setting: PersonalComputeSetting, field_mask: str) -> PersonalComputeSetting

        Update Personal Compute setting.
        
        Updates the value of the Personal Compute setting.
        
        :param allow_missing: bool
          This should always be set to true for Settings API. Added for AIP compliance.
        :param setting: :class:`PersonalComputeSetting`
        :param field_mask: str
          Field mask is required to be passed into the PATCH request. Field mask specifies which fields of the
          setting payload will be updated. The field mask needs to be supplied as single string. To specify
          multiple fields in the field mask, use comma as the separator (no space).
        
        :returns: :class:`PersonalComputeSetting`
        