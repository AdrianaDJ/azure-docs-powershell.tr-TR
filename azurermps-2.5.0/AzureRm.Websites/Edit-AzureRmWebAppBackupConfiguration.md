---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/edit-azurermwebappbackupconfiguration
schema: 2.0.0
ms.openlocfilehash: 9a90e56909de016bb388be1a43f5b41c8e47e9e8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939037"
---
# <span data-ttu-id="ad4fa-101">Edit-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad4fa-101">Edit-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="ad4fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad4fa-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad4fa-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ad4fa-103">SYNTAX</span></span>

### <span data-ttu-id="ad4fa-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="ad4fa-104">FromResourceName</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="ad4fa-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="ad4fa-105">FromWebApp</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="ad4fa-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="ad4fa-106">DESCRIPTION</span></span>
<span data-ttu-id="ad4fa-107">**Edit-AzureRmWebAppBackupConfiguration** cmdlet 'ı Azure Web App için geçerli yapılandırma yedeklemesini düzenler.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-107">The **Edit-AzureRmWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="ad4fa-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ad4fa-108">EXAMPLES</span></span>

## <span data-ttu-id="ad4fa-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ad4fa-109">PARAMETERS</span></span>

### <span data-ttu-id="ad4fa-110">-Veritabanları</span><span class="sxs-lookup"><span data-stu-id="ad4fa-110">-Databases</span></span>
<span data-ttu-id="ad4fa-111">DatabaseBackupSetting [] türündeki veritabanları</span><span class="sxs-lookup"><span data-stu-id="ad4fa-111">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad4fa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad4fa-112">-DefaultProfile</span></span>
<span data-ttu-id="ad4fa-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad4fa-114">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="ad4fa-114">-FrequencyInterval</span></span>
<span data-ttu-id="ad4fa-115">Frekans aralığı</span><span class="sxs-lookup"><span data-stu-id="ad4fa-115">Frequency Interval</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad4fa-116">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="ad4fa-116">-FrequencyUnit</span></span>
<span data-ttu-id="ad4fa-117">Frekans birimi</span><span class="sxs-lookup"><span data-stu-id="ad4fa-117">Frequency Unit</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad4fa-118">-Nepatleastonebackup</span><span class="sxs-lookup"><span data-stu-id="ad4fa-118">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="ad4fa-119">En az bir yedekleme seçeneği tutma</span><span class="sxs-lookup"><span data-stu-id="ad4fa-119">Keep At Least One Backup Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad4fa-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="ad4fa-120">-Name</span></span>
<span data-ttu-id="ad4fa-121">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="ad4fa-121">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad4fa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad4fa-122">-ResourceGroupName</span></span>
<span data-ttu-id="ad4fa-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="ad4fa-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad4fa-124">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="ad4fa-124">-RetentionPeriodInDays</span></span>
<span data-ttu-id="ad4fa-125">Gün cinsinden bekletme süresi</span><span class="sxs-lookup"><span data-stu-id="ad4fa-125">Retention Period In Days</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad4fa-126">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="ad4fa-126">-Slot</span></span>
<span data-ttu-id="ad4fa-127">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="ad4fa-127">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad4fa-128">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="ad4fa-128">-StartTime</span></span>
<span data-ttu-id="ad4fa-129">UTC 'deki başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="ad4fa-129">StartTime in UTC</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad4fa-130">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="ad4fa-130">-StorageAccountUrl</span></span>
<span data-ttu-id="ad4fa-131">Depolama hesabı URL 'Si</span><span class="sxs-lookup"><span data-stu-id="ad4fa-131">Storage Account Url</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad4fa-132">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ad4fa-132">-WebApp</span></span>
<span data-ttu-id="ad4fa-133">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="ad4fa-133">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad4fa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad4fa-134">CommonParameters</span></span>
<span data-ttu-id="ad4fa-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad4fa-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad4fa-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad4fa-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ad4fa-137">INPUTS</span></span>

### <span data-ttu-id="ad4fa-138">Bölge</span><span class="sxs-lookup"><span data-stu-id="ad4fa-138">Site</span></span>
<span data-ttu-id="ad4fa-139">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="ad4fa-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="ad4fa-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ad4fa-140">OUTPUTS</span></span>

### <span data-ttu-id="ad4fa-141">Microsoft. Azure. Commands. WebApps. cmdlet. WebApps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad4fa-141">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="ad4fa-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ad4fa-142">NOTES</span></span>

## <span data-ttu-id="ad4fa-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ad4fa-143">RELATED LINKS</span></span>

[<span data-ttu-id="ad4fa-144">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad4fa-144">Get-AzureRmWebAppBackupConfiguration</span></span>](./Get-AzureRmWebAppBackupConfiguration.md)


