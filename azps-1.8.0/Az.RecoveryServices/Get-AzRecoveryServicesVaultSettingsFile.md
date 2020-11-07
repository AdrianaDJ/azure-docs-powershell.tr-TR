---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: 5455babba58e050397066e5439b3e046315b4101
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759680"
---
# <span data-ttu-id="0c1f4-101">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="0c1f4-101">Get-AzRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="0c1f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c1f4-102">SYNOPSIS</span></span>
<span data-ttu-id="0c1f4-103">Azure Site Recovery kasa ayarları dosyasını alır.</span><span class="sxs-lookup"><span data-stu-id="0c1f4-103">Gets the Azure Site Recovery vault settings file.</span></span>

## <span data-ttu-id="0c1f4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0c1f4-104">SYNTAX</span></span>

### <span data-ttu-id="0c1f4-105">ForSiteWithCertificate</span><span class="sxs-lookup"><span data-stu-id="0c1f4-105">ForSiteWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -SiteIdentifier <String>
 -Certificate <String> -SiteFriendlyName <String> [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0c1f4-106">ByDefaultWithCertificate</span><span class="sxs-lookup"><span data-stu-id="0c1f4-106">ByDefaultWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String>
 [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c1f4-107">ForBackupVaultTypeWithCertificate</span><span class="sxs-lookup"><span data-stu-id="0c1f4-107">ForBackupVaultTypeWithCertificate</span></span>
```
Get-AzRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] -Certificate <String> [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c1f4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0c1f4-108">DESCRIPTION</span></span>
<span data-ttu-id="0c1f4-109">**Get-Azrecoveryservicesvaultsettingsfıle** cmdlet 'i, bir Azure Site Recovery Kasası için ayarlar dosyasını alır.</span><span class="sxs-lookup"><span data-stu-id="0c1f4-109">The **Get-AzRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="0c1f4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0c1f4-110">EXAMPLES</span></span>

### <span data-ttu-id="0c1f4-111">Örnek 1: Azure yedekleme için Windows Server veya DPM makinesini kaydettirme</span><span class="sxs-lookup"><span data-stu-id="0c1f4-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="0c1f4-112">İlk komut Testkasası adlı kasayı alır ve $Vault 01 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="0c1f4-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="0c1f4-113">İkinci komut $CredsPath değişkenini C:\downloadolarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="0c1f4-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>
<span data-ttu-id="0c1f4-114">Son komut, Azure yedekleme için $CredsPath 'daki kimlik bilgilerini kullanarak $Vault 01 kasa kimlik bilgileri dosyasını alır.</span><span class="sxs-lookup"><span data-stu-id="0c1f4-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

### <span data-ttu-id="0c1f4-115">Örnek 2:</span><span class="sxs-lookup"><span data-stu-id="0c1f4-115">Example 2:</span></span>
```
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="0c1f4-116">Komut $Vault 01 kasa türü siteRecovery için kasa kimlik bilgileri dosyasını alır.</span><span class="sxs-lookup"><span data-stu-id="0c1f4-116">The command gets the vault credentials file for $Vault01 of vault type siteRecovery.</span></span>

### <span data-ttu-id="0c1f4-117">Örnek 3: Azure yedekleme için Windows Server veya DPM makinesini kaydettirme</span><span class="sxs-lookup"><span data-stu-id="0c1f4-117">Example 3: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Credsfilename = Get-AzRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="0c1f4-118">Komut $Vault 01 için kasa kimlik bilgileri dosyasını alır.</span><span class="sxs-lookup"><span data-stu-id="0c1f4-118">The command gets the vault credentials file for $Vault01.</span></span>

## <span data-ttu-id="0c1f4-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0c1f4-119">PARAMETERS</span></span>

### <span data-ttu-id="0c1f4-120">-Yedekleme</span><span class="sxs-lookup"><span data-stu-id="0c1f4-120">-Backup</span></span>
<span data-ttu-id="0c1f4-121">Kasa kimlik bilgileri dosyasının Azure yedekleme 'ye uygun olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="0c1f4-121">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForBackupVaultTypeWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c1f4-122">-Sertifika</span><span class="sxs-lookup"><span data-stu-id="0c1f4-122">-Certificate</span></span>
<span data-ttu-id="0c1f4-123">{{Sertifikayı doldur açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="0c1f4-123">{{Fill Certificate Description}}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c1f4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c1f4-124">-DefaultProfile</span></span>
<span data-ttu-id="0c1f4-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0c1f4-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c1f4-126">-Yol</span><span class="sxs-lookup"><span data-stu-id="0c1f4-126">-Path</span></span>
<span data-ttu-id="0c1f4-127">Azure Site Recovery kasa ayarları dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c1f4-127">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="0c1f4-128">Bu dosyayı Azure Site Recovery kasa portalından indirebilir ve yerel olarak depolayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0c1f4-128">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c1f4-129">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="0c1f4-129">-SiteFriendlyName</span></span>
<span data-ttu-id="0c1f4-130">Sitenin kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c1f4-130">Specifies the site friendly name.</span></span>
<span data-ttu-id="0c1f4-131">Bir Hyper-V sitesinin kasa kimlik bilgilerini indiriyorsunuz bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="0c1f4-131">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSiteWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c1f4-132">-Sitetanımlayıcısı</span><span class="sxs-lookup"><span data-stu-id="0c1f4-132">-SiteIdentifier</span></span>
<span data-ttu-id="0c1f4-133">Site tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c1f4-133">Specifies the site identifier.</span></span>
<span data-ttu-id="0c1f4-134">Bir Hyper-V sitesinin kasa kimlik bilgilerini indiriyorsunuz bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="0c1f4-134">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSiteWithCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c1f4-135">-Siterecoçok</span><span class="sxs-lookup"><span data-stu-id="0c1f4-135">-SiteRecovery</span></span>
<span data-ttu-id="0c1f4-136">Kasa kimlik bilgileri dosyasının Azure Site Recovery için geçerli olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="0c1f4-136">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForSiteWithCertificate, ByDefaultWithCertificate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c1f4-137">-Kasa</span><span class="sxs-lookup"><span data-stu-id="0c1f4-137">-Vault</span></span>
<span data-ttu-id="0c1f4-138">Azure Site Recovery kasa nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c1f4-138">Specifies the Azure Site Recovery vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c1f4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c1f4-139">CommonParameters</span></span>
<span data-ttu-id="0c1f4-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0c1f4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c1f4-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c1f4-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c1f4-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0c1f4-142">INPUTS</span></span>

### <span data-ttu-id="0c1f4-143">Microsoft. Azure. Commands. RecoveryServices. Arskasa</span><span class="sxs-lookup"><span data-stu-id="0c1f4-143">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="0c1f4-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0c1f4-144">OUTPUTS</span></span>

### <span data-ttu-id="0c1f4-145">Microsoft. Azure. Commands. RecoveryServices. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="0c1f4-145">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="0c1f4-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0c1f4-146">NOTES</span></span>

## <span data-ttu-id="0c1f4-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0c1f4-147">RELATED LINKS</span></span>

[<span data-ttu-id="0c1f4-148">Get-Azrecoveryserviceskasa</span><span class="sxs-lookup"><span data-stu-id="0c1f4-148">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="0c1f4-149">Yeni-Azrecoveryserviceskasası</span><span class="sxs-lookup"><span data-stu-id="0c1f4-149">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="0c1f4-150">Remove-Azrecoveryserviceskasa</span><span class="sxs-lookup"><span data-stu-id="0c1f4-150">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


