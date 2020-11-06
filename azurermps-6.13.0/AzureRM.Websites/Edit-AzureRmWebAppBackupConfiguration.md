---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: BFC38930-DBB4-4EBB-8E29-73B901FAF486
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/edit-azurermwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Edit-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Edit-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: a7a66197752e7dd9ec58e7eeca921af277687ed2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587093"
---
# <span data-ttu-id="ff89a-101">Edit-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff89a-101">Edit-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="ff89a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff89a-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff89a-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ff89a-103">SYNTAX</span></span>

### <span data-ttu-id="ff89a-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="ff89a-104">FromResourceName</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="ff89a-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="ff89a-105">FromWebApp</span></span>
```
Edit-AzureRmWebAppBackupConfiguration [-FrequencyInterval] <Int32> [-FrequencyUnit] <String>
 [-RetentionPeriodInDays] <Int32> [[-StartTime] <DateTime>] [-KeepAtLeastOneBackup] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [[-Databases] <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="ff89a-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="ff89a-106">DESCRIPTION</span></span>
<span data-ttu-id="ff89a-107">**Edit-AzureRmWebAppBackupConfiguration** cmdlet 'ı Azure Web App için geçerli yapılandırma yedeklemesini düzenler.</span><span class="sxs-lookup"><span data-stu-id="ff89a-107">The **Edit-AzureRmWebAppBackupConfiguration** cmdlet edits the current configuration backup for an Azure Web App.</span></span>

## <span data-ttu-id="ff89a-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ff89a-108">EXAMPLES</span></span>

## <span data-ttu-id="ff89a-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ff89a-109">PARAMETERS</span></span>

### <span data-ttu-id="ff89a-110">-Veritabanları</span><span class="sxs-lookup"><span data-stu-id="ff89a-110">-Databases</span></span>
<span data-ttu-id="ff89a-111">DatabaseBackupSetting [] türündeki veritabanları</span><span class="sxs-lookup"><span data-stu-id="ff89a-111">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="ff89a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff89a-112">-DefaultProfile</span></span>
<span data-ttu-id="ff89a-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ff89a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff89a-114">-FrequencyInterval</span><span class="sxs-lookup"><span data-stu-id="ff89a-114">-FrequencyInterval</span></span>
<span data-ttu-id="ff89a-115">Frekans aralığı</span><span class="sxs-lookup"><span data-stu-id="ff89a-115">Frequency Interval</span></span>

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

### <span data-ttu-id="ff89a-116">-FrequencyUnit</span><span class="sxs-lookup"><span data-stu-id="ff89a-116">-FrequencyUnit</span></span>
<span data-ttu-id="ff89a-117">Frekans birimi</span><span class="sxs-lookup"><span data-stu-id="ff89a-117">Frequency Unit</span></span>

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

### <span data-ttu-id="ff89a-118">-Nepatleastonebackup</span><span class="sxs-lookup"><span data-stu-id="ff89a-118">-KeepAtLeastOneBackup</span></span>
<span data-ttu-id="ff89a-119">En az bir yedekleme seçeneği tutma</span><span class="sxs-lookup"><span data-stu-id="ff89a-119">Keep At Least One Backup Option</span></span>

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

### <span data-ttu-id="ff89a-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="ff89a-120">-Name</span></span>
<span data-ttu-id="ff89a-121">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="ff89a-121">WebApp Name</span></span>

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

### <span data-ttu-id="ff89a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff89a-122">-ResourceGroupName</span></span>
<span data-ttu-id="ff89a-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="ff89a-123">Resource Group Name</span></span>

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

### <span data-ttu-id="ff89a-124">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="ff89a-124">-RetentionPeriodInDays</span></span>
<span data-ttu-id="ff89a-125">Gün cinsinden bekletme süresi</span><span class="sxs-lookup"><span data-stu-id="ff89a-125">Retention Period In Days</span></span>

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

### <span data-ttu-id="ff89a-126">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="ff89a-126">-Slot</span></span>
<span data-ttu-id="ff89a-127">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="ff89a-127">WebApp Slot Name</span></span>

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

### <span data-ttu-id="ff89a-128">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="ff89a-128">-StartTime</span></span>
<span data-ttu-id="ff89a-129">UTC 'deki başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="ff89a-129">StartTime in UTC</span></span>

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

### <span data-ttu-id="ff89a-130">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="ff89a-130">-StorageAccountUrl</span></span>
<span data-ttu-id="ff89a-131">Depolama hesabı URL 'Si</span><span class="sxs-lookup"><span data-stu-id="ff89a-131">Storage Account Url</span></span>

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

### <span data-ttu-id="ff89a-132">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ff89a-132">-WebApp</span></span>
<span data-ttu-id="ff89a-133">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="ff89a-133">WebApp Object</span></span>

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

### <span data-ttu-id="ff89a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff89a-134">CommonParameters</span></span>
<span data-ttu-id="ff89a-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ff89a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff89a-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff89a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff89a-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ff89a-137">INPUTS</span></span>

### <span data-ttu-id="ff89a-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ff89a-138">System.Int32</span></span>

### <span data-ttu-id="ff89a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ff89a-139">System.String</span></span>

### <span data-ttu-id="ff89a-140">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="ff89a-140">System.DateTime</span></span>

### <span data-ttu-id="ff89a-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ff89a-141">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="ff89a-142">Microsoft. Azure. Management. Web sitesi. modeller. site</span><span class="sxs-lookup"><span data-stu-id="ff89a-142">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="ff89a-143">Parametreler: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ff89a-143">Parameters: WebApp (ByValue)</span></span>

### <span data-ttu-id="ff89a-144">Microsoft. Azure. Management. Web sitesi. modeller. DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="ff89a-144">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

## <span data-ttu-id="ff89a-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ff89a-145">OUTPUTS</span></span>

### <span data-ttu-id="ff89a-146">Microsoft. Azure. Commands. WebApps. cmdlet. WebApps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff89a-146">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="ff89a-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ff89a-147">NOTES</span></span>

## <span data-ttu-id="ff89a-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ff89a-148">RELATED LINKS</span></span>

[<span data-ttu-id="ff89a-149">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff89a-149">Get-AzureRmWebAppBackupConfiguration</span></span>](./Get-AzureRmWebAppBackupConfiguration.md)


