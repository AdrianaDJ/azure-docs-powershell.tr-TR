---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/edit-Azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
ms.openlocfilehash: cfac8f1cd3d25ff630900bb5d7723e713b3d4c65
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936132"
---
# <span data-ttu-id="7547c-101">Edit-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="7547c-101">Edit-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="7547c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7547c-102">SYNOPSIS</span></span>

## <span data-ttu-id="7547c-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7547c-103">SYNTAX</span></span>

### <span data-ttu-id="7547c-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="7547c-104">FromResourceName</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="7547c-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="7547c-105">FromWebApp</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="7547c-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="7547c-106">DESCRIPTION</span></span>
<span data-ttu-id="7547c-107">**Edit-AzWebAppBackupConfiguration** cmdlet 'ı Azure Web App için geçerli yapılandırma yedeklemesini düzenler.</span><span class="sxs-lookup"><span data-stu-id="7547c-107">The **Edit-AzWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="7547c-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7547c-108">EXAMPLES</span></span>

## <span data-ttu-id="7547c-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7547c-109">PARAMETERS</span></span>

### <span data-ttu-id="7547c-110">-Veritabanları</span><span class="sxs-lookup"><span data-stu-id="7547c-110">-Databases</span></span>
<span data-ttu-id="7547c-111">DatabaseBackupSetting [] türündeki veritabanları</span><span class="sxs-lookup"><span data-stu-id="7547c-111">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="7547c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7547c-112">-DefaultProfile</span></span>
<span data-ttu-id="7547c-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7547c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7547c-114">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="7547c-114">-FrequencyInterval</span></span>
<span data-ttu-id="7547c-115">Frekans aralığı</span><span class="sxs-lookup"><span data-stu-id="7547c-115">Frequency Interval</span></span>

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

### <span data-ttu-id="7547c-116">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="7547c-116">-FrequencyUnit</span></span>
<span data-ttu-id="7547c-117">Frekans birimi</span><span class="sxs-lookup"><span data-stu-id="7547c-117">Frequency Unit</span></span>

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

### <span data-ttu-id="7547c-118">-Nepatleastonebackup</span><span class="sxs-lookup"><span data-stu-id="7547c-118">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="7547c-119">En az bir yedekleme seçeneği tutma</span><span class="sxs-lookup"><span data-stu-id="7547c-119">Keep At Least One Backup Option</span></span>

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

### <span data-ttu-id="7547c-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="7547c-120">-Name</span></span>
<span data-ttu-id="7547c-121">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="7547c-121">WebApp Name</span></span>

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

### <span data-ttu-id="7547c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7547c-122">-ResourceGroupName</span></span>
<span data-ttu-id="7547c-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="7547c-123">Resource Group Name</span></span>

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

### <span data-ttu-id="7547c-124">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="7547c-124">-RetentionPeriodInDays</span></span>
<span data-ttu-id="7547c-125">Gün cinsinden bekletme süresi</span><span class="sxs-lookup"><span data-stu-id="7547c-125">Retention Period In Days</span></span>

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

### <span data-ttu-id="7547c-126">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="7547c-126">-Slot</span></span>
<span data-ttu-id="7547c-127">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="7547c-127">WebApp Slot Name</span></span>

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

### <span data-ttu-id="7547c-128">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="7547c-128">-StartTime</span></span>
<span data-ttu-id="7547c-129">UTC 'deki başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="7547c-129">StartTime in UTC</span></span>

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

### <span data-ttu-id="7547c-130">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="7547c-130">-StorageAccountUrl</span></span>
<span data-ttu-id="7547c-131">Depolama hesabı URL 'Si</span><span class="sxs-lookup"><span data-stu-id="7547c-131">Storage Account Url</span></span>

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

### <span data-ttu-id="7547c-132">-WebApp</span><span class="sxs-lookup"><span data-stu-id="7547c-132">-WebApp</span></span>
<span data-ttu-id="7547c-133">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="7547c-133">WebApp Object</span></span>

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

### <span data-ttu-id="7547c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7547c-134">CommonParameters</span></span>
<span data-ttu-id="7547c-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7547c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7547c-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7547c-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7547c-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7547c-137">INPUTS</span></span>

### <span data-ttu-id="7547c-138">Bölge</span><span class="sxs-lookup"><span data-stu-id="7547c-138">Site</span></span>
<span data-ttu-id="7547c-139">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="7547c-139">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="7547c-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7547c-140">OUTPUTS</span></span>

### <span data-ttu-id="7547c-141">Microsoft. Azure. Commands. WebApps. cmdlet. WebApps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="7547c-141">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="7547c-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7547c-142">NOTES</span></span>

## <span data-ttu-id="7547c-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7547c-143">RELATED LINKS</span></span>

[<span data-ttu-id="7547c-144">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="7547c-144">Get-AzWebAppBackupConfiguration</span></span>](./Get-AzWebAppBackupConfiguration.md)


