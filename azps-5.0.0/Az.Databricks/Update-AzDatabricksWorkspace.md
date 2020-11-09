---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/update-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksWorkspace.md
ms.openlocfilehash: 0d213dd18ea2423c90dec6446e4551cbcd8d161a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320201"
---
# <span data-ttu-id="08125-101">Update-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="08125-101">Update-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="08125-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08125-102">SYNOPSIS</span></span>
<span data-ttu-id="08125-103">Çalışma alanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="08125-103">Updates a workspace.</span></span>

## <span data-ttu-id="08125-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="08125-104">SYNTAX</span></span>

### <span data-ttu-id="08125-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="08125-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyName <String>] [-EncryptionKeySource <KeySource>] [-EncryptionKeyVaultUri <String>]
 [-EncryptionKeyVersion <String>] [-PrepareEncryption] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="08125-106">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="08125-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-EncryptionKeyName <String>]
 [-EncryptionKeySource <KeySource>] [-EncryptionKeyVaultUri <String>] [-EncryptionKeyVersion <String>]
 [-PrepareEncryption] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="08125-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="08125-107">DESCRIPTION</span></span>
<span data-ttu-id="08125-108">Çalışma alanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="08125-108">Updates a workspace.</span></span>

## <span data-ttu-id="08125-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="08125-109">EXAMPLES</span></span>

### <span data-ttu-id="08125-110">Örnek 1: Veriricks çalışma alanının etiketlerini güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="08125-110">Example 1: Updates the tags of a Databricks workspace</span></span>
```powershell
PS C:\> $dbr = Get-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceopsc46 -Tag @{'key'=1}
PS C:\> Update-AzDatabricksWorkspace -InputObject $dbr -Tag @{key="value"}

Name            Location Managed Resource Group ID
----            -------- -------------------------
workspaceopsc46 eastus   /subscriptions/0140911e-1040-48da-8bc9-b99fb3dd88a6/resourceGroups/databricks-rg-workspaceopsc46-wfgp3ayhu6jkn
```

<span data-ttu-id="08125-111">Bu komut, Veriricks çalışma alanının etiketlerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="08125-111">This command updates the tags of a Databricks workspace.</span></span>

### <span data-ttu-id="08125-112">Örnek 2: Veriricks çalışma alanında şifrelemeyi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="08125-112">Example 2: Enable encryption on a Databricks workspace</span></span>
```powershell
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -PrepareEncryption
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -EncryptionKeySource 'Microsoft.KeyVault' -EncryptionKeyVaultUri https://keyvalult-j3kube.vault.azure.net/ -EncryptionKeyName key-p3bjsf -EncryptionKeyVersion 853999da89714fb4a1408681945135fd

Name            Location       Managed Resource Group ID
----            --------       -------------------------
workspaceypae6l East US 2 EUAP /subscriptions/0140911e-1040-48da-8bc9-b99fb3dd88a6/resourceGroups/databricks-rg-workspaceypae6l-wzefrgv2b075t
```

<span data-ttu-id="08125-113">Databricks çalışma alanında şifrelemeyi etkinleştirmek üç adımdan yararlanır:</span><span class="sxs-lookup"><span data-stu-id="08125-113">Enabling encryption on a Databricks workspace takes three steps:</span></span>
1.
<span data-ttu-id="08125-114">Çalışma alanını `-PrepareEncryption` (henüz oluşturmadıysanız) güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="08125-114">Update the workspace with `-PrepareEncryption` (if it was not created so).</span></span>
1.
<span data-ttu-id="08125-115">`StorageAccountIdentityPrincipalId`Son adımın çıktısında bulun.</span><span class="sxs-lookup"><span data-stu-id="08125-115">Find `StorageAccountIdentityPrincipalId` in the output of the last step.</span></span>
<span data-ttu-id="08125-116">Sorumluya anahtar izinleri verin.</span><span class="sxs-lookup"><span data-stu-id="08125-116">Grant key permissions to the principal.</span></span>
1.
<span data-ttu-id="08125-117">Şifreleme anahtarıyla ilgili bilgileri doldurmak için çalışma alanını yeniden güncelleyin:</span><span class="sxs-lookup"><span data-stu-id="08125-117">Update the workspace again to fill in information about the encryption key:</span></span>
    - `-EncryptionKeySource`
    - `-EncryptionKeyVaultUri`
    - `-EncryptionKeyName`
    - `-EncryptionKeyVersion`

### <span data-ttu-id="08125-118">Örnek 3: Veriricks çalışma alanında şifrelemeyi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="08125-118">Example 3: Disable encryption on a Databricks workspace</span></span>
```powershell
PS C:\> Update-AzDatabricksWorkspace -ResourceGroupName databricks-rg-952d47 -Name workspaceypae6l -EncryptionKeySource 'Default'
```

<span data-ttu-id="08125-119">Şifrelemeyi devre dışı bırakmak için, seçeneğini ayarlayın `-EncryptionKeySource` `'Default'` .</span><span class="sxs-lookup"><span data-stu-id="08125-119">To disable encryption, simply set `-EncryptionKeySource` to `'Default'`.</span></span>

## <span data-ttu-id="08125-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="08125-120">PARAMETERS</span></span>

### <span data-ttu-id="08125-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="08125-121">-AsJob</span></span>
<span data-ttu-id="08125-122">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="08125-122">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08125-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08125-123">-DefaultProfile</span></span>
<span data-ttu-id="08125-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="08125-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08125-125">-Encryptionanahtaradı</span><span class="sxs-lookup"><span data-stu-id="08125-125">-EncryptionKeyName</span></span>
<span data-ttu-id="08125-126">Anahtar kasa anahtarının adı.</span><span class="sxs-lookup"><span data-stu-id="08125-126">The name of Key Vault key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08125-127">-EncryptionKeySource</span><span class="sxs-lookup"><span data-stu-id="08125-127">-EncryptionKeySource</span></span>
<span data-ttu-id="08125-128">Şifreleme keySource (sağlayıcı).</span><span class="sxs-lookup"><span data-stu-id="08125-128">The encryption keySource (provider).</span></span>
<span data-ttu-id="08125-129">Olası değerler (büyük/küçük harf duyarsız): varsayılan, Microsoft. Keykasa</span><span class="sxs-lookup"><span data-stu-id="08125-129">Possible values (case-insensitive): Default, Microsoft.Keyvault</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Support.KeySource
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08125-130">-Şifrelemeklavye</span><span class="sxs-lookup"><span data-stu-id="08125-130">-EncryptionKeyVaultUri</span></span>
<span data-ttu-id="08125-131">Anahtar Kasası URI 'SI (DNS adı).</span><span class="sxs-lookup"><span data-stu-id="08125-131">The URI (DNS name) of the Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08125-132">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="08125-132">-EncryptionKeyVersion</span></span>
<span data-ttu-id="08125-133">Keykasa anahtarının sürümü.</span><span class="sxs-lookup"><span data-stu-id="08125-133">The version of KeyVault key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08125-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08125-134">-InputObject</span></span>
<span data-ttu-id="08125-135">Kimlik parametresi.</span><span class="sxs-lookup"><span data-stu-id="08125-135">Identity parameter.</span></span>
<span data-ttu-id="08125-136">Oluşturmak için, ıNPUTOBJECT özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="08125-136">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08125-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="08125-137">-Name</span></span>
<span data-ttu-id="08125-138">Çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="08125-138">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08125-139">-NoWait</span><span class="sxs-lookup"><span data-stu-id="08125-139">-NoWait</span></span>
<span data-ttu-id="08125-140">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="08125-140">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08125-141">-PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="08125-141">-PrepareEncryption</span></span>
<span data-ttu-id="08125-142">Çalışma alanını şifreleme için hazırlayın.</span><span class="sxs-lookup"><span data-stu-id="08125-142">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="08125-143">Yönetilen depolama hesabı için yönetilen kimliği etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="08125-143">Enables the Managed Identity for managed storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08125-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08125-144">-ResourceGroupName</span></span>
<span data-ttu-id="08125-145">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="08125-145">The name of the resource group.</span></span>
<span data-ttu-id="08125-146">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="08125-146">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08125-147">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="08125-147">-SubscriptionId</span></span>
<span data-ttu-id="08125-148">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="08125-148">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08125-149">Etiketli</span><span class="sxs-lookup"><span data-stu-id="08125-149">-Tag</span></span>
<span data-ttu-id="08125-150">Kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="08125-150">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08125-151">-Onay</span><span class="sxs-lookup"><span data-stu-id="08125-151">-Confirm</span></span>
<span data-ttu-id="08125-152">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="08125-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08125-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08125-153">-WhatIf</span></span>
<span data-ttu-id="08125-154">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="08125-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08125-155">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="08125-155">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08125-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08125-156">CommonParameters</span></span>
<span data-ttu-id="08125-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="08125-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08125-158">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="08125-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08125-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="08125-159">INPUTS</span></span>

### <span data-ttu-id="08125-160">Microsoft. Azure. PowerShell. cmdlet. Veriricks. model. ıdatabricksıdentity</span><span class="sxs-lookup"><span data-stu-id="08125-160">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="08125-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="08125-161">OUTPUTS</span></span>

### <span data-ttu-id="08125-162">Microsoft. Azure. PowerShell. cmdlet. Veriricks. modeller. Api20180401. ıworkspace</span><span class="sxs-lookup"><span data-stu-id="08125-162">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="08125-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="08125-163">NOTES</span></span>

<span data-ttu-id="08125-164">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="08125-164">ALIASES</span></span>

<span data-ttu-id="08125-165">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="08125-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="08125-166">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="08125-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="08125-167">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="08125-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="08125-168">INPUTOBJECT <IDatabricksIdentity> : IDENTITY parametresi.</span><span class="sxs-lookup"><span data-stu-id="08125-168">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="08125-169">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="08125-169">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="08125-170">`[PeeringName <String>]`: Çalışma alanı vNet eşlemesi adı.</span><span class="sxs-lookup"><span data-stu-id="08125-170">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="08125-171">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="08125-171">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="08125-172">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="08125-172">The name is case insensitive.</span></span>
  - <span data-ttu-id="08125-173">`[SubscriptionId <String>]`: Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="08125-173">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="08125-174">`[WorkspaceName <String>]`: Çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="08125-174">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="08125-175">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="08125-175">RELATED LINKS</span></span>

