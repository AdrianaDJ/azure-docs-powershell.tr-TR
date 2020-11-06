---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/edit-azurermwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Edit-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Edit-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: 9c23484fa5f8b45548985645db45872fcc63f66b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592852"
---
# <span data-ttu-id="cea4a-101">Edit-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="cea4a-101">Edit-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="cea4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cea4a-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cea4a-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cea4a-103">SYNTAX</span></span>

### <span data-ttu-id="cea4a-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="cea4a-104">FromResourceName</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="cea4a-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="cea4a-105">FromWebApp</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="cea4a-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="cea4a-106">DESCRIPTION</span></span>
<span data-ttu-id="cea4a-107">**Edit-AzureRmWebAppBackupConfiguration** cmdlet 'ı Azure Web App için geçerli yapılandırma yedeklemesini düzenler.</span><span class="sxs-lookup"><span data-stu-id="cea4a-107">The **Edit-AzureRmWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="cea4a-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cea4a-108">EXAMPLES</span></span>

## <span data-ttu-id="cea4a-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cea4a-109">PARAMETERS</span></span>

### <span data-ttu-id="cea4a-110">-Veritabanları</span><span class="sxs-lookup"><span data-stu-id="cea4a-110">-Databases</span></span>
<span data-ttu-id="cea4a-111">DatabaseBackupSetting [] türündeki veritabanları</span><span class="sxs-lookup"><span data-stu-id="cea4a-111">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="cea4a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cea4a-112">-DefaultProfile</span></span>
<span data-ttu-id="cea4a-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cea4a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cea4a-114">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="cea4a-114">-FrequencyInterval</span></span>
<span data-ttu-id="cea4a-115">Frekans aralığı</span><span class="sxs-lookup"><span data-stu-id="cea4a-115">Frequency Interval</span></span>

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

### <span data-ttu-id="cea4a-116">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="cea4a-116">-FrequencyUnit</span></span>
<span data-ttu-id="cea4a-117">Frekans birimi</span><span class="sxs-lookup"><span data-stu-id="cea4a-117">Frequency Unit</span></span>

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

### <span data-ttu-id="cea4a-118">-Nepatleastonebackup</span><span class="sxs-lookup"><span data-stu-id="cea4a-118">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="cea4a-119">En az bir yedekleme seçeneği tutma</span><span class="sxs-lookup"><span data-stu-id="cea4a-119">Keep At Least One Backup Option</span></span>

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

### <span data-ttu-id="cea4a-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="cea4a-120">-Name</span></span>
<span data-ttu-id="cea4a-121">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="cea4a-121">WebApp Name</span></span>

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

### <span data-ttu-id="cea4a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cea4a-122">-ResourceGroupName</span></span>
<span data-ttu-id="cea4a-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="cea4a-123">Resource Group Name</span></span>

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

### <span data-ttu-id="cea4a-124">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="cea4a-124">-RetentionPeriodInDays</span></span>
<span data-ttu-id="cea4a-125">Gün cinsinden bekletme süresi</span><span class="sxs-lookup"><span data-stu-id="cea4a-125">Retention Period In Days</span></span>

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

### <span data-ttu-id="cea4a-126">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="cea4a-126">-Slot</span></span>
<span data-ttu-id="cea4a-127">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="cea4a-127">WebApp Slot Name</span></span>

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

### <span data-ttu-id="cea4a-128">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="cea4a-128">-StartTime</span></span>
<span data-ttu-id="cea4a-129">UTC 'deki başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="cea4a-129">StartTime in UTC</span></span>

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

### <span data-ttu-id="cea4a-130">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="cea4a-130">-StorageAccountUrl</span></span>
<span data-ttu-id="cea4a-131">Depolama hesabı URL 'Si</span><span class="sxs-lookup"><span data-stu-id="cea4a-131">Storage Account Url</span></span>

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

### <span data-ttu-id="cea4a-132">-WebApp</span><span class="sxs-lookup"><span data-stu-id="cea4a-132">-WebApp</span></span>
<span data-ttu-id="cea4a-133">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="cea4a-133">WebApp Object</span></span>

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

### <span data-ttu-id="cea4a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cea4a-134">CommonParameters</span></span>
<span data-ttu-id="cea4a-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cea4a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cea4a-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cea4a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cea4a-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cea4a-137">INPUTS</span></span>

### <span data-ttu-id="cea4a-138">Bölge</span><span class="sxs-lookup"><span data-stu-id="cea4a-138">Site</span></span>
<span data-ttu-id="cea4a-139">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="cea4a-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="cea4a-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cea4a-140">OUTPUTS</span></span>

### <span data-ttu-id="cea4a-141">Microsoft. Azure. Commands. WebApps. cmdlet. WebApps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="cea4a-141">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="cea4a-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cea4a-142">NOTES</span></span>

## <span data-ttu-id="cea4a-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cea4a-143">RELATED LINKS</span></span>

[<span data-ttu-id="cea4a-144">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="cea4a-144">Get-AzureRmWebAppBackupConfiguration</span></span>](./Get-AzureRmWebAppBackupConfiguration.md)


