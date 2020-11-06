---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: a0572e73d270a37b3c705018a38b4a88fe88d1e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593917"
---
# <span data-ttu-id="01d9f-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="01d9f-101">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>

## <span data-ttu-id="01d9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01d9f-102">SYNOPSIS</span></span>
<span data-ttu-id="01d9f-103">Azure Site Recovery kasa ayarları dosyasını alır.</span><span class="sxs-lookup"><span data-stu-id="01d9f-103">Gets the Azure Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01d9f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="01d9f-104">SYNTAX</span></span>

### <span data-ttu-id="01d9f-105">Forsıte</span><span class="sxs-lookup"><span data-stu-id="01d9f-105">ForSite</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> -SiteIdentifier <String>
 -SiteFriendlyName <String> [[-Path] <String>] [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="01d9f-106">ByDefault</span><span class="sxs-lookup"><span data-stu-id="01d9f-106">ByDefault</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-SiteRecovery]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01d9f-107">ForBackupVaultType</span><span class="sxs-lookup"><span data-stu-id="01d9f-107">ForBackupVaultType</span></span>
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01d9f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="01d9f-108">DESCRIPTION</span></span>
<span data-ttu-id="01d9f-109">**Get-Azurermrecoveryservicesvaultsettingsfıle** cmdlet 'i, bir Azure Site Recovery Kasası için ayarlar dosyasını alır.</span><span class="sxs-lookup"><span data-stu-id="01d9f-109">The **Get-AzureRmRecoveryServicesVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="01d9f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="01d9f-110">EXAMPLES</span></span>

### <span data-ttu-id="01d9f-111">Örnek 1: Azure yedekleme için Windows Server veya DPM makinesini kaydettirme</span><span class="sxs-lookup"><span data-stu-id="01d9f-111">Example 1: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

<span data-ttu-id="01d9f-112">İlk komut Testkasası adlı kasayı alır ve $Vault 01 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="01d9f-112">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="01d9f-113">İkinci komut $CredsPath değişkenini C:\downloadolarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="01d9f-113">The second command sets the $CredsPath variable to C:\Downloads.</span></span>
<span data-ttu-id="01d9f-114">Son komut, Azure yedekleme için $CredsPath 'daki kimlik bilgilerini kullanarak $Vault 01 kasa kimlik bilgileri dosyasını alır.</span><span class="sxs-lookup"><span data-stu-id="01d9f-114">The last command gets the vault credentials file for $Vault01 using the credentials in $CredsPath for Azure Backup.</span></span>

### <span data-ttu-id="01d9f-115">Örnek 2:</span><span class="sxs-lookup"><span data-stu-id="01d9f-115">Example 2:</span></span>
```
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="01d9f-116">Komut $Vault 01 kasa türü siteRecovery için kasa kimlik bilgileri dosyasını alır.</span><span class="sxs-lookup"><span data-stu-id="01d9f-116">The command gets the vault credentials file for $Vault01 of vault type siteRecovery.</span></span>

### <span data-ttu-id="01d9f-117">Örnek 3: Azure yedekleme için Windows Server veya DPM makinesini kaydettirme</span><span class="sxs-lookup"><span data-stu-id="01d9f-117">Example 3: Register a Windows Server or DPM machine for Azure Backup</span></span>
```
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -SiteIdentifier -Vault $Vault01
```

<span data-ttu-id="01d9f-118">Komut $Vault 01 için kasa kimlik bilgileri dosyasını alır.</span><span class="sxs-lookup"><span data-stu-id="01d9f-118">The command gets the vault credentials file for $Vault01.</span></span>

## <span data-ttu-id="01d9f-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="01d9f-119">PARAMETERS</span></span>

### <span data-ttu-id="01d9f-120">-Yedekleme</span><span class="sxs-lookup"><span data-stu-id="01d9f-120">-Backup</span></span>
<span data-ttu-id="01d9f-121">Kasa kimlik bilgileri dosyasının Azure yedekleme 'ye uygun olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="01d9f-121">Indicates the vault credentials file is applicable to Azure Backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForBackupVaultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01d9f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01d9f-122">-DefaultProfile</span></span>
<span data-ttu-id="01d9f-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="01d9f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01d9f-124">-Yol</span><span class="sxs-lookup"><span data-stu-id="01d9f-124">-Path</span></span>
<span data-ttu-id="01d9f-125">Azure Site Recovery kasa ayarları dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="01d9f-125">Specifies the path to the Azure Site Recovery vault settings file.</span></span>
<span data-ttu-id="01d9f-126">Bu dosyayı Azure Site Recovery kasa portalından indirebilir ve yerel olarak depolayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="01d9f-126">You can download this file from the Azure Site Recovery vault portal and store it locally.</span></span>

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

### <span data-ttu-id="01d9f-127">-SiteFriendlyName</span><span class="sxs-lookup"><span data-stu-id="01d9f-127">-SiteFriendlyName</span></span>
<span data-ttu-id="01d9f-128">Sitenin kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="01d9f-128">Specifies the site friendly name.</span></span>
<span data-ttu-id="01d9f-129">Bir Hyper-V sitesinin kasa kimlik bilgilerini indiriyorsunuz bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="01d9f-129">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSite
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01d9f-130">-Sitetanımlayıcısı</span><span class="sxs-lookup"><span data-stu-id="01d9f-130">-SiteIdentifier</span></span>
<span data-ttu-id="01d9f-131">Site tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="01d9f-131">Specifies the site identifier.</span></span>
<span data-ttu-id="01d9f-132">Bir Hyper-V sitesinin kasa kimlik bilgilerini indiriyorsunuz bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="01d9f-132">Use this parameter if you are downloading the vault credentials for a Hyper-V site.</span></span>

```yaml
Type: System.String
Parameter Sets: ForSite
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01d9f-133">-Siterecoçok</span><span class="sxs-lookup"><span data-stu-id="01d9f-133">-SiteRecovery</span></span>
<span data-ttu-id="01d9f-134">Kasa kimlik bilgileri dosyasının Azure Site Recovery için geçerli olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="01d9f-134">Indicates the vault credentials file is applicable to Azure Site Recovery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForSite, ByDefault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01d9f-135">-Kasa</span><span class="sxs-lookup"><span data-stu-id="01d9f-135">-Vault</span></span>
<span data-ttu-id="01d9f-136">Azure Site Recovery kasa nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="01d9f-136">Specifies the Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="01d9f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01d9f-137">CommonParameters</span></span>
<span data-ttu-id="01d9f-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="01d9f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01d9f-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01d9f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01d9f-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="01d9f-140">INPUTS</span></span>

### <span data-ttu-id="01d9f-141">Microsoft. Azure. Commands. RecoveryServices. Arskasa</span><span class="sxs-lookup"><span data-stu-id="01d9f-141">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>
<span data-ttu-id="01d9f-142">Parametreler: kasa (ByValue)</span><span class="sxs-lookup"><span data-stu-id="01d9f-142">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="01d9f-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="01d9f-143">OUTPUTS</span></span>

### <span data-ttu-id="01d9f-144">Microsoft. Azure. Commands. RecoveryServices. VaultSettingsFilePath</span><span class="sxs-lookup"><span data-stu-id="01d9f-144">Microsoft.Azure.Commands.RecoveryServices.VaultSettingsFilePath</span></span>

## <span data-ttu-id="01d9f-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="01d9f-145">NOTES</span></span>

## <span data-ttu-id="01d9f-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="01d9f-146">RELATED LINKS</span></span>

[<span data-ttu-id="01d9f-147">Get-Azurermrecoveryserviceskasası</span><span class="sxs-lookup"><span data-stu-id="01d9f-147">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="01d9f-148">Yeni-Azurermrecoveryserviceskasası</span><span class="sxs-lookup"><span data-stu-id="01d9f-148">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="01d9f-149">Remove-Azurermrecoveryserviceskasası</span><span class="sxs-lookup"><span data-stu-id="01d9f-149">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


