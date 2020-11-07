---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 5bd0e525607180659365c81825d6ad6899578fae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752691"
---
# <span data-ttu-id="2044f-101">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="2044f-101">Set-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="2044f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2044f-102">SYNOPSIS</span></span>
<span data-ttu-id="2044f-103">Azure 'da çalışan bir IaaS sanal makinesinde şifrelemeyi mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="2044f-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

## <span data-ttu-id="2044f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2044f-104">SYNTAX</span></span>

### <span data-ttu-id="2044f-105">SinglePassParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2044f-105">SinglePassParameterSet (Default)</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>] [[-VolumeType] <String>]
 [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>] [[-Passphrase] <String>]
 [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2044f-106">AADClientSecretParameterSet</span><span class="sxs-lookup"><span data-stu-id="2044f-106">AADClientSecretParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2044f-107">AADClientCertParameterSet</span><span class="sxs-lookup"><span data-stu-id="2044f-107">AADClientCertParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2044f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2044f-108">DESCRIPTION</span></span>
<span data-ttu-id="2044f-109">**Set-AzVMDiskEncryptionExtension** cmdlet 'i, çalışan bir altyapıda Azure 'da hizmet (IaaS) sanal makinesi olarak şifrelemeyi olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="2044f-109">The **Set-AzVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>  <span data-ttu-id="2044f-110">Sanal makineye disk şifrelemesi uzantısını yükleyerek şifrelemeyi mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="2044f-110">It enables encryption by installing the disk encryption extension on the virtual machine.</span></span> 

<span data-ttu-id="2044f-111">Bu cmdlet, şifrelemeyi etkinleştirme adımlarının sanal makinenin yeniden başlatılmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="2044f-111">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>

<span data-ttu-id="2044f-112">Bu cmdlet 'i çalıştırmadan önce çalışmanızı sanal makinede kaydetmeniz tavsiye edilir.</span><span class="sxs-lookup"><span data-stu-id="2044f-112">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

<span data-ttu-id="2044f-113">Linux: Linux sanal makineler şifrelenirken **Volumetype** parametresi gereklidir ve Linux dağılımının desteklediği bir değer ("OS", "Data" veya "All") olarak ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2044f-113">Linux: The **VolumeType** parameter is required when encrypting Linux virtual machines, and must be set to a value ("Os", "Data", or "All") supported by the Linux distribution.</span></span> 

<span data-ttu-id="2044f-114">Windows: **Volumetype** parametresi atlanabilir; bu durumda işlem tümü için varsayılan olarak; Windows sanal makinesi için Birimtürü parametresi varsa, tümü veya işletim sistemine ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2044f-114">Windows: The **VolumeType** parameter may be omitted, in which case the operation defaults to All; if the VolumeType parameter is present for a Windows virtual machine, it must be set to either All or OS.</span></span>

## <span data-ttu-id="2044f-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2044f-115">EXAMPLES</span></span>

### <span data-ttu-id="2044f-116">Örnek 1: şifrelemeyi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="2044f-116">Example 1: Enable encryption</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="2044f-117">Bu örnek, AD kimlik bilgilerini belirtmeden bir VM 'de şifrelemeyi olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="2044f-117">This example enables encryption on a VM without specifying AD credentials.</span></span>

### <span data-ttu-id="2044f-118">Örnek 2: ardışık düzen girişiyle şifrelemeyi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="2044f-118">Example 2: Enable encryption with pipelined input</span></span>
```
$params = New-Object PSObject -Property @{
    ResourceGroupName = "[resource-group-name]"
    VMName = "[vm-name]"
    DiskEncryptionKeyVaultId = "/subscriptions/[subscription-id-guid]/resourceGroups/[resource-group-name]/providers/Microsoft.KeyVault/vaults/[keyvault-name]"
    DiskEncryptionKeyVaultUrl = "https://[keyvault-name].vault.azure.net"
    KeyEncryptionKeyVaultId = "/subscriptions/[subscription-id-guid]/resourceGroups/[resource-group-name]/providers/Microsoft.KeyVault/vaults/[keyvault-name]"
    KeyEncryptionKeyUrl = "https://[keyvault-name].vault.azure.net/keys/[kekname]/[kek-unique-id]"
    VolumeType = "All"
}

$params | Set-AzVmDiskEncryptionExtension
```

<span data-ttu-id="2044f-119">Bu örnek, AD kimlik bilgilerini belirtmeden bir VM 'de şifrelemeyi etkinleştirmek için ardışık düzen kullanan girişleri kullanarak parametreleri gönderir.</span><span class="sxs-lookup"><span data-stu-id="2044f-119">This example sends parameters using pipelined input to enable encryption on a VM, without specifying AD credentials.</span></span>

### <span data-ttu-id="2044f-120">Örnek 3: Azure AD Istemci KIMLIĞINI ve Istemci gizliliğini kullanarak şifrelemeyi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="2044f-120">Example 3: Enable encryption using Azure AD Client ID and Client Secret</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="2044f-121">Bu örnekte, bir VM 'de şifrelemeyi etkinleştirmek için Azure AD istemci KIMLIĞI ve istemci parolası kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2044f-121">This example uses Azure AD client ID and client secret to enable encryption on a VM.</span></span>

### <span data-ttu-id="2044f-122">Örnek 4: Azure AD İstemci KIMLIĞINI ve istemci sertifikası parmak izini kullanarak şifrelemeyi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="2044f-122">Example 4: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$CertValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -CertValue $CertValue 
$ServicePrincipal = New-AzADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

$AADClientID = $AzureAdApplication.ApplicationId
$aadClientCertThumbprint= $cert.Thumbprint

#Upload pfx to KeyVault 
$KeyVaultSecretName = "MyAADCert"
$FileContentBytes = get-content $CertPath -Encoding Byte
$FileContentEncoded = [System.Convert]::ToBase64String($fileContentBytes)
$JSONObject = @"
    { 
        "data" : "$filecontentencoded", 
        "dataType" : "pfx", 
        "password" : "$CertPassword" 
    } 
"@
$JSONObjectBytes = [System.Text.Encoding]::UTF8.GetBytes($jsonObject)
$JSONEncoded = [System.Convert]::ToBase64String($jsonObjectBytes)

$Secret = ConvertTo-SecureString -String $JSONEncoded -AsPlainText -Force
Set-AzKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName -SecretValue $Secret
Set-AzKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl
Update-AzVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="2044f-123">Bu örnekte, bir VM 'de şifrelemeyi etkinleştirmek için Azure AD istemci KIMLIĞI ve istemci sertifikası parmak izleri kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="2044f-123">This example uses Azure AD client ID and client certification thumbprints to enable encryption on a VM.</span></span>

### <span data-ttu-id="2044f-124">Örnek 5: anahtar şifreleme anahtarını kullanarak Azure AD istemci KIMLIĞI, istemci parolası kullanarak şifrelemeyi etkinleştirme ve disk şifrelemesini sarma</span><span class="sxs-lookup"><span data-stu-id="2044f-124">Example 5: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"

$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"

$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"

$KEKName = "MyKeyEncryptionKey"
$KEK = Add-AzKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="2044f-125">Bu örnekte, bir VM 'de şifrelemeyi etkinleştirmek için Azure AD istemci KIMLIĞI ve istemci parolası kullanılır ve disk şifrelemesi anahtarı anahtar şifreleme anahtarı kullanılarak kaydırılır.</span><span class="sxs-lookup"><span data-stu-id="2044f-125">This example uses Azure AD client ID and client secret to enable encryption on a VM, and wraps the disk encryption key using a key encryption key.</span></span>

### <span data-ttu-id="2044f-126">Örnek 6: anahtar şifreleme anahtarı kullanarak Azure AD istemci KIMLIĞI, istemci sertifikası parmak izi ve disk şifrelemesi</span><span class="sxs-lookup"><span data-stu-id="2044f-126">Example 6: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$KEKName = "MyKeyEncryptionKey"
$KEK = Add-AzKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid
$VolumeType = "All"

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$CertValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -CertValue $CertValue
$ServicePrincipal = New-AzADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

$AADClientID = $AzureAdApplication.ApplicationId
$AADClientCertThumbprint= $Cert.Thumbprint

#Upload pfx to KeyVault 
$KeyVaultSecretName = "MyAADCert"
$FileContentBytes = get-content $CertPath -Encoding Byte
$FileContentEncoded = [System.Convert]::ToBase64String($FileContentBytes)
$JSONObject = @"
    { 
        "data" : "$filecontentencoded", 
        "dataType" : "pfx", 
        "password" : "$CertPassword" 
    } 
"@
$JSONObjectBytes = [System.Text.Encoding]::UTF8.GetBytes($JSONObject)
$JsonEncoded = [System.Convert]::ToBase64String($JSONObjectBytes)
$Secret = ConvertTo-SecureString -String $JSONEncoded -AsPlainText -Force
Set-AzKeyVaultSecret -VaultName $VaultName-Name $KeyVaultSecretName -SecretValue $Secret
Set-AzKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl 
Update-AzVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGname -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="2044f-127">Bu örnekte, bir VM 'de şifrelemeyi etkinleştirmek için Azure AD istemci KIMLIĞI ve istemci sertifikası parmak izi kullanılır ve disk şifrelemesi anahtarı anahtar şifreleme anahtarı kullanılarak kaydırılır.</span><span class="sxs-lookup"><span data-stu-id="2044f-127">This example uses Azure AD client ID and client cert thumbprint to enable encryption on a VM, and wraps the disk encryption key using a key encryption key.</span></span>

## <span data-ttu-id="2044f-128">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2044f-128">PARAMETERS</span></span>

### <span data-ttu-id="2044f-129">-Aadclientcertparmak Izi</span><span class="sxs-lookup"><span data-stu-id="2044f-129">-AadClientCertThumbprint</span></span>
<span data-ttu-id="2044f-130">**Anahtar kasaya** gizli yazma Izinleri olan AzureActive Directory (Azure AD) uygulama istemcisi sertifikasının parmak izini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2044f-130">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="2044f-131">Önkoşul olarak, Azure AD İstemcisi sertifikasının daha önce sanal makinenin yerel bilgisayar `my` sertifika deposuna dağıtılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="2044f-131">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="2044f-132">Azure 'daki bir sanal makineye sertifika dağıtmak için Add-AzVMSecret cmdlet 'i kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="2044f-132">The Add-AzVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="2044f-133">Daha fazla bilgi için **Add-AzVMSecret** cmdlet yardımına bakın.</span><span class="sxs-lookup"><span data-stu-id="2044f-133">For more details, see the **Add-AzVMSecret** cmdlet help.</span></span>
<span data-ttu-id="2044f-134">Sertifika, daha önce sanal makine yerel bilgisayarına sertifika deponuza dağıtılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2044f-134">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

```yaml
Type: System.String
Parameter Sets: AADClientCertParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2044f-135">-Aadclitıd</span><span class="sxs-lookup"><span data-stu-id="2044f-135">-AadClientID</span></span>
<span data-ttu-id="2044f-136">**Anahtar kasaya** gizli yazma Izni olan Azure AD UYGULAMASıNıN istemci kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2044f-136">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: System.String
Parameter Sets: AADClientSecretParameterSet, AADClientCertParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2044f-137">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="2044f-137">-AadClientSecret</span></span>
<span data-ttu-id="2044f-138">**Anahtar kasaya** parola yazma Izinleri olan Azure AD uygulamasının istemci gizliliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2044f-138">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: System.String
Parameter Sets: AADClientSecretParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2044f-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2044f-139">-DefaultProfile</span></span>
<span data-ttu-id="2044f-140">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2044f-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2044f-141">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="2044f-141">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="2044f-142">Bu cmdlet 'in, uzantının ara sürümünün otomatik yükseltmesini devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2044f-142">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2044f-143">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="2044f-143">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="2044f-144">Sanal makine şifreleme anahtarlarının karşıya yüklenmesi gereken **tuş Kasası** kaynak kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2044f-144">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2044f-145">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="2044f-145">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="2044f-146">Sanal makine şifreleme anahtarlarının karşıya yüklenmesi gereken **tuş Kasası** URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2044f-146">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2044f-147">-EncryptFormatAll</span><span class="sxs-lookup"><span data-stu-id="2044f-147">-EncryptFormatAll</span></span>
<span data-ttu-id="2044f-148">Şifrelenmemiş olan tüm veri sürücülerini Encrypt-Format</span><span class="sxs-lookup"><span data-stu-id="2044f-148">Encrypt-Format all data drives that are not already encrypted</span></span>

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

### <span data-ttu-id="2044f-149">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="2044f-149">-ExtensionPublisherName</span></span>
<span data-ttu-id="2044f-150">Dahili yayımcı adı.</span><span class="sxs-lookup"><span data-stu-id="2044f-150">The extension publisher name.</span></span> <span data-ttu-id="2044f-151">Bu parametreyi yalnızca "Microsoft. Azure. Security" varsayılan değerini geçersiz kılmak için belirtin.</span><span class="sxs-lookup"><span data-stu-id="2044f-151">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2044f-152">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="2044f-152">-ExtensionType</span></span>
<span data-ttu-id="2044f-153">Uzantı türü.</span><span class="sxs-lookup"><span data-stu-id="2044f-153">The extension type.</span></span> <span data-ttu-id="2044f-154">Windows VM 'ler için "AzureDiskEncryption" varsayılan değerini (Linux VM 'Ler için "AzureDiskEncryptionForLinux" olarak geçersiz kılmak için bu parametreyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="2044f-154">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2044f-155">-Force</span><span class="sxs-lookup"><span data-stu-id="2044f-155">-Force</span></span>
<span data-ttu-id="2044f-156">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="2044f-156">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2044f-157">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="2044f-157">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="2044f-158">Sanal makinenin anahtar şifrelemesini kaydırmak ve kaydırmak için kullanılan algoritmayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="2044f-158">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="2044f-159">Varsayılan değer RSA-OAEP.</span><span class="sxs-lookup"><span data-stu-id="2044f-159">The default value is RSA-OAEP.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA1_5

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2044f-160">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="2044f-160">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="2044f-161">Sanal makine şifreleme anahtarını kaydırmak ve kaydırmak için kullanılan anahtar şifreleme anahtarının URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2044f-161">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="2044f-162">Bu, tam sürümlü URL olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2044f-162">This must be the full versioned URL.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2044f-163">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="2044f-163">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="2044f-164">Sanal makine şifreleme anahtarını kaydırmak ve kaydırmak için kullanılan anahtar şifreleme anahtarını içeren tuş **Kasası** kaynak kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2044f-164">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="2044f-165">Bu, tam sürümlü bir URL olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2044f-165">This must be a full versioned URL.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2044f-166">-Ad</span><span class="sxs-lookup"><span data-stu-id="2044f-166">-Name</span></span>
<span data-ttu-id="2044f-167">Uzantıyı temsil eden Azure Resource Manager kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2044f-167">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span> <span data-ttu-id="2044f-168">*Name* parametresi atlanırsa, yüklü uzantı Windows sanal makinelerinde AzureDiskEncryption olarak adlandırılacaktır ve Linux sanal makinelerinde AzureDiskEncryptionForLinux.</span><span class="sxs-lookup"><span data-stu-id="2044f-168">If the *Name* parameter is omitted, the installed extension will be named AzureDiskEncryption on Windows virtual machines and AzureDiskEncryptionForLinux on Linux virtual machines.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2044f-169">-Parola</span><span class="sxs-lookup"><span data-stu-id="2044f-169">-Passphrase</span></span>
<span data-ttu-id="2044f-170">Linux sanal makinelerini şifrelemek için kullanılan parolayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="2044f-170">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="2044f-171">Bu parametre, Windows işletim sistemini çalıştıran sanal makinelerde kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="2044f-171">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2044f-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2044f-172">-ResourceGroupName</span></span>
<span data-ttu-id="2044f-173">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2044f-173">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2044f-174">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="2044f-174">-SequenceVersion</span></span>
<span data-ttu-id="2044f-175">Sanal makine için şifreleme işlemlerinin dizi sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2044f-175">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="2044f-176">Bu, aynı sanal makinede gerçekleştirilen her şifreleme işlemi için benzersizdir.</span><span class="sxs-lookup"><span data-stu-id="2044f-176">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="2044f-177">Get-AzVMExtension cmdlet, kullanılan önceki seri numarasını almak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="2044f-177">The Get-AzVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2044f-178">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="2044f-178">-SkipVmBackup</span></span>
<span data-ttu-id="2044f-179">Linux VM 'Ler için yedekleme oluşturmayı atlama</span><span class="sxs-lookup"><span data-stu-id="2044f-179">Skip backup creation for Linux VMs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2044f-180">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="2044f-180">-TypeHandlerVersion</span></span>
<span data-ttu-id="2044f-181">Şifreleme uzantısının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="2044f-181">Specifies the version of the encryption extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2044f-182">-VMName</span><span class="sxs-lookup"><span data-stu-id="2044f-182">-VMName</span></span>
<span data-ttu-id="2044f-183">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2044f-183">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2044f-184">-Birimtürü</span><span class="sxs-lookup"><span data-stu-id="2044f-184">-VolumeType</span></span>
<span data-ttu-id="2044f-185">Şifreleme işleminin gerçekleştirileceği sanal makine birimlerinin türünü belirtir: işletim sistemi, veri veya tümü.</span><span class="sxs-lookup"><span data-stu-id="2044f-185">Specifies the type of virtual machine volumes on which to perform encryption operation: OS, Data, or All.</span></span> 

<span data-ttu-id="2044f-186">Linux: Linux sanal makineler şifrelenirken **Volumetype** parametresi gereklidir ve Linux dağılımının desteklediği bir değer ("OS", "Data" veya "All") olarak ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2044f-186">Linux: The **VolumeType** parameter is required when encrypting Linux virtual machines, and must be set to a value ("Os", "Data", or "All") supported by the Linux distribution.</span></span> 

<span data-ttu-id="2044f-187">Windows: **Volumetype** parametresi atlanabilir; bu durumda işlem tümü için varsayılan olarak; Windows sanal makinesi için Birimtürü parametresi varsa, tümü veya işletim sistemine ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2044f-187">Windows: The **VolumeType** parameter may be omitted, in which case the operation defaults to All; if the VolumeType parameter is present for a Windows virtual machine, it must be set to either All or OS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2044f-188">-Onay</span><span class="sxs-lookup"><span data-stu-id="2044f-188">-Confirm</span></span>
<span data-ttu-id="2044f-189">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2044f-189">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2044f-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2044f-190">-WhatIf</span></span>
<span data-ttu-id="2044f-191">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2044f-191">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2044f-192">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2044f-192">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2044f-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2044f-193">CommonParameters</span></span>
<span data-ttu-id="2044f-194">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2044f-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2044f-195">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2044f-195">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2044f-196">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2044f-196">INPUTS</span></span>

### <span data-ttu-id="2044f-197">System. String</span><span class="sxs-lookup"><span data-stu-id="2044f-197">System.String</span></span>

### <span data-ttu-id="2044f-198">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2044f-198">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2044f-199">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2044f-199">OUTPUTS</span></span>

### <span data-ttu-id="2044f-200">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2044f-200">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="2044f-201">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2044f-201">NOTES</span></span>

## <span data-ttu-id="2044f-202">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2044f-202">RELATED LINKS</span></span>

[<span data-ttu-id="2044f-203">Add-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="2044f-203">Add-AzVMSecret</span></span>](./Add-AzVMSecret.md)

[<span data-ttu-id="2044f-204">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="2044f-204">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="2044f-205">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="2044f-205">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)


