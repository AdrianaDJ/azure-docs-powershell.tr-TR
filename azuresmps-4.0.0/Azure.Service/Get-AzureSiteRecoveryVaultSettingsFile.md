---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: AFAA1BDF-3F6A-437A-ADC2-C5EBD970F57D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94e86fdb7f1e995af71e09bdce17754b11819bec
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106564"
---
# <span data-ttu-id="1e860-101">Get-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="1e860-101">Get-AzureSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="1e860-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e860-102">SYNOPSIS</span></span>
<span data-ttu-id="1e860-103">Site Recovery kasa ayarları dosyasını alır.</span><span class="sxs-lookup"><span data-stu-id="1e860-103">Gets the Site Recovery vault settings file.</span></span>

## <span data-ttu-id="1e860-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1e860-104">SYNTAX</span></span>

### <span data-ttu-id="1e860-105">ByParam (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1e860-105">ByParam (Default)</span></span>
```
Get-AzureSiteRecoveryVaultSettingsFile -Name <String> -Location <String> [-SiteName <String>]
 [-SiteId <String>] [-Path <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1e860-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="1e860-106">ByObject</span></span>
```
Get-AzureSiteRecoveryVaultSettingsFile -Vault <ASRVault> [-Site <ASRSite>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="1e860-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1e860-107">DESCRIPTION</span></span>
<span data-ttu-id="1e860-108">**Get-AzureSiteRecoveryVaultSettingsFile** cmdlet 'ı bir Azure Site Recovery Kasası için ayarlar dosyasını alır.</span><span class="sxs-lookup"><span data-stu-id="1e860-108">The **Get-AzureSiteRecoveryVaultSettingsFile** cmdlet gets the settings file for an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="1e860-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1e860-109">EXAMPLES</span></span>

### <span data-ttu-id="1e860-110">Örnek 1: kasa için ayarlar dosyasını alma</span><span class="sxs-lookup"><span data-stu-id="1e860-110">Example 1: Get the settings file for a vault</span></span>
```
PS C:\> $Vault = Get-AzureSiteRecoveryVault -Name "ContosoVault"
PS C:\> Get-AzureSiteRecoveryVaultSettingsFile -Vault $Vault
FilePath 
-------- 
C:\Users\ContosoAdmin\ContosoVault_2015-02-02T05-39-23.VaultCredentials
```

<span data-ttu-id="1e860-111">İlk komut, **Get-AzureSiteRecoveryVault** cmdlet 'Ini kullanarak contosokasası adlı etkin Azure Site kurtarma kasasından yararlanalır.</span><span class="sxs-lookup"><span data-stu-id="1e860-111">The first command gets the active Azure Site Recovery vault named ContosoVault by using the **Get-AzureSiteRecoveryVault** cmdlet.</span></span>
<span data-ttu-id="1e860-112">Komut bu kasayı $Vault değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="1e860-112">The command stores that vault in the $Vault variable.</span></span>

<span data-ttu-id="1e860-113">İkinci komut $Vault 'de depolanan kasanın ayarlar dosyasını alır.</span><span class="sxs-lookup"><span data-stu-id="1e860-113">The second command gets the settings file for the vault stored in $Vault.</span></span>

## <span data-ttu-id="1e860-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1e860-114">PARAMETERS</span></span>

### <span data-ttu-id="1e860-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="1e860-115">-Location</span></span>
<span data-ttu-id="1e860-116">Kasanın ait olduğu coğrafi konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e860-116">Specifies the geographical location to which the vault belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e860-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="1e860-117">-Name</span></span>
<span data-ttu-id="1e860-118">Kasanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e860-118">Specifies the name of a vault.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e860-119">-Yol</span><span class="sxs-lookup"><span data-stu-id="1e860-119">-Path</span></span>
<span data-ttu-id="1e860-120">Site Recovery kasa ayarları dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e860-120">Specifies the path of the Site Recovery vault settings file.</span></span>
<span data-ttu-id="1e860-121">Bu dosyayı yerel olarak depolamak için, komutun çalışması bittiğinde site kurtarma Kasası portalından indirin.</span><span class="sxs-lookup"><span data-stu-id="1e860-121">To store this file locally, download it from the Site Recovery vault portal after the command has finished running.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e860-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="1e860-122">-Profile</span></span>
<span data-ttu-id="1e860-123">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e860-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1e860-124">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="1e860-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e860-125">-Site</span><span class="sxs-lookup"><span data-stu-id="1e860-125">-Site</span></span>
<span data-ttu-id="1e860-126">Ayarlar dosyası alınacak bir site belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e860-126">Specifies a site for which to get a settings file.</span></span>
<span data-ttu-id="1e860-127">**Site** nesnesi edinmek için **Get-AzureSiteRecoverySite** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1e860-127">To obtain a **Site** object, use the **Get-AzureSiteRecoverySite** cmdlet.</span></span>

```yaml
Type: ASRSite
Parameter Sets: ByObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e860-128">-Sitekimliği</span><span class="sxs-lookup"><span data-stu-id="1e860-128">-SiteId</span></span>
<span data-ttu-id="1e860-129">Sitenin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e860-129">Specifies the ID of a site.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e860-130">-SiteName</span><span class="sxs-lookup"><span data-stu-id="1e860-130">-SiteName</span></span>
<span data-ttu-id="1e860-131">Sitenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e860-131">Specifies the name of a site.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e860-132">-Kasa</span><span class="sxs-lookup"><span data-stu-id="1e860-132">-Vault</span></span>
<span data-ttu-id="1e860-133">Sitenin kasasıyla ilgili.</span><span class="sxs-lookup"><span data-stu-id="1e860-133">Specifies the vault for the site.</span></span>

```yaml
Type: ASRVault
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e860-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e860-134">CommonParameters</span></span>
<span data-ttu-id="1e860-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1e860-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e860-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e860-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e860-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1e860-137">INPUTS</span></span>

## <span data-ttu-id="1e860-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1e860-138">OUTPUTS</span></span>

## <span data-ttu-id="1e860-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1e860-139">NOTES</span></span>

## <span data-ttu-id="1e860-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1e860-140">RELATED LINKS</span></span>

[<span data-ttu-id="1e860-141">Get-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="1e860-141">Get-AzureSiteRecoverySite</span></span>](./Get-AzureSiteRecoverySite.md)

[<span data-ttu-id="1e860-142">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="1e860-142">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)

[<span data-ttu-id="1e860-143">Get-AzureSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="1e860-143">Get-AzureSiteRecoveryVaultSettings</span></span>](./Get-AzureSiteRecoveryVaultSettings.md)

[<span data-ttu-id="1e860-144">İçeri aktarma-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="1e860-144">Import-AzureSiteRecoveryVaultSettingsFile</span></span>](./Import-AzureSiteRecoveryVaultSettingsFile.md)


