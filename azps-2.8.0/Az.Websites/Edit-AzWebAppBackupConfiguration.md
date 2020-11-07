---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/edit-azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Edit-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 4319a2637b2dbb008056a6b369ace539b889cd37
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934381"
---
# <span data-ttu-id="bb300-101">Edit-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="bb300-101">Edit-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="bb300-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb300-102">SYNOPSIS</span></span>

## <span data-ttu-id="bb300-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bb300-103">SYNTAX</span></span>

### <span data-ttu-id="bb300-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="bb300-104">FromResourceName</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="bb300-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="bb300-105">FromWebApp</span></span>
```
Edit-AzWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="bb300-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="bb300-106">DESCRIPTION</span></span>
<span data-ttu-id="bb300-107">**Edit-AzWebAppBackupConfiguration** cmdlet 'ı Azure Web App için geçerli yapılandırma yedeklemesini düzenler.</span><span class="sxs-lookup"><span data-stu-id="bb300-107">The **Edit-AzWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="bb300-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bb300-108">EXAMPLES</span></span>

## <span data-ttu-id="bb300-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bb300-109">PARAMETERS</span></span>

### <span data-ttu-id="bb300-110">-Veritabanları</span><span class="sxs-lookup"><span data-stu-id="bb300-110">-Databases</span></span>
<span data-ttu-id="bb300-111">DatabaseBackupSetting [] türündeki veritabanları</span><span class="sxs-lookup"><span data-stu-id="bb300-111">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb300-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb300-112">-DefaultProfile</span></span>
<span data-ttu-id="bb300-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bb300-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb300-114">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="bb300-114">-FrequencyInterval</span></span>
<span data-ttu-id="bb300-115">Frekans aralığı</span><span class="sxs-lookup"><span data-stu-id="bb300-115">Frequency Interval</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb300-116">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="bb300-116">-FrequencyUnit</span></span>
<span data-ttu-id="bb300-117">Frekans birimi</span><span class="sxs-lookup"><span data-stu-id="bb300-117">Frequency Unit</span></span>

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

### <span data-ttu-id="bb300-118">-Nepatleastonebackup</span><span class="sxs-lookup"><span data-stu-id="bb300-118">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="bb300-119">En az bir yedekleme seçeneği tutma</span><span class="sxs-lookup"><span data-stu-id="bb300-119">Keep At Least One Backup Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb300-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="bb300-120">-Name</span></span>
<span data-ttu-id="bb300-121">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="bb300-121">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb300-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb300-122">-ResourceGroupName</span></span>
<span data-ttu-id="bb300-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="bb300-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb300-124">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="bb300-124">-RetentionPeriodInDays</span></span>
<span data-ttu-id="bb300-125">Gün cinsinden bekletme süresi</span><span class="sxs-lookup"><span data-stu-id="bb300-125">Retention Period In Days</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb300-126">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="bb300-126">-Slot</span></span>
<span data-ttu-id="bb300-127">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="bb300-127">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb300-128">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="bb300-128">-StartTime</span></span>
<span data-ttu-id="bb300-129">UTC 'deki başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="bb300-129">StartTime in UTC</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb300-130">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="bb300-130">-StorageAccountUrl</span></span>
<span data-ttu-id="bb300-131">Depolama hesabı URL 'Si</span><span class="sxs-lookup"><span data-stu-id="bb300-131">Storage Account Url</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb300-132">-WebApp</span><span class="sxs-lookup"><span data-stu-id="bb300-132">-WebApp</span></span>
<span data-ttu-id="bb300-133">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="bb300-133">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb300-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb300-134">CommonParameters</span></span>
<span data-ttu-id="bb300-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bb300-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb300-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb300-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb300-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bb300-137">INPUTS</span></span>

### <span data-ttu-id="bb300-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="bb300-138">System.Int32</span></span>

### <span data-ttu-id="bb300-139">System. String</span><span class="sxs-lookup"><span data-stu-id="bb300-139">System.String</span></span>

### <span data-ttu-id="bb300-140">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="bb300-140">System.DateTime</span></span>

### <span data-ttu-id="bb300-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bb300-141">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="bb300-142">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="bb300-142">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="bb300-143">Microsoft. Azure. Management. Web sitesi. modeller. DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="bb300-143">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

## <span data-ttu-id="bb300-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bb300-144">OUTPUTS</span></span>

### <span data-ttu-id="bb300-145">Microsoft. Azure. Commands. WebApps. cmdlet. WebApps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="bb300-145">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="bb300-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bb300-146">NOTES</span></span>

## <span data-ttu-id="bb300-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bb300-147">RELATED LINKS</span></span>

[<span data-ttu-id="bb300-148">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="bb300-148">Get-AzWebAppBackupConfiguration</span></span>](./Get-AzWebAppBackupConfiguration.md)


