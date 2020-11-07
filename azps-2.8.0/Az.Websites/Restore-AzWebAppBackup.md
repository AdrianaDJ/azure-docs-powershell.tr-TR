---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppBackup.md
ms.openlocfilehash: 94fbc71db34ca0abc6a27130dc166318794e271a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934126"
---
# <span data-ttu-id="22491-101">Restore-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="22491-101">Restore-AzWebAppBackup</span></span>

## <span data-ttu-id="22491-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22491-102">SYNOPSIS</span></span>

## <span data-ttu-id="22491-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="22491-103">SYNTAX</span></span>

### <span data-ttu-id="22491-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="22491-104">FromResourceName</span></span>
```
Restore-AzWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite]
 [<CommonParameters>]
```

### <span data-ttu-id="22491-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="22491-105">FromWebApp</span></span>
```
Restore-AzWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="22491-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="22491-106">DESCRIPTION</span></span>
<span data-ttu-id="22491-107">**Restore-AzWebAppBackup** cmdlet 'ı Azure Web App yedeklemesini geri yükler.</span><span class="sxs-lookup"><span data-stu-id="22491-107">The **Restore-AzWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="22491-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="22491-108">EXAMPLES</span></span>

### <span data-ttu-id="22491-109">2</span><span class="sxs-lookup"><span data-stu-id="22491-109">1:</span></span>
```
PS C:\> Restore-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="22491-110">Belirtilen uygulamanın bir yedeğini geri yükler kaynak grubu içinde varsayılan-Web-WestUS https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="22491-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="22491-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="22491-111">PARAMETERS</span></span>

### <span data-ttu-id="22491-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="22491-112">-AppServicePlan</span></span>
<span data-ttu-id="22491-113">Geri yüklenen uygulama için App Service planının adı.</span><span class="sxs-lookup"><span data-stu-id="22491-113">The name of the App Service Plan for the restored app.</span></span> <span data-ttu-id="22491-114">Boş bırakılırsa uygulamanın geçerli App Service planı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="22491-114">If left empty, the app's current App Service Plan is used.</span></span>

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

### <span data-ttu-id="22491-115">-BlobName</span><span class="sxs-lookup"><span data-stu-id="22491-115">-BlobName</span></span>
<span data-ttu-id="22491-116">Blob adı</span><span class="sxs-lookup"><span data-stu-id="22491-116">Blob Name</span></span>

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

### <span data-ttu-id="22491-117">-Veritabanları</span><span class="sxs-lookup"><span data-stu-id="22491-117">-Databases</span></span>
<span data-ttu-id="22491-118">DatabaseBackupSetting [] türündeki veritabanları</span><span class="sxs-lookup"><span data-stu-id="22491-118">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22491-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22491-119">-DefaultProfile</span></span>
<span data-ttu-id="22491-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="22491-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22491-121">-Ignoreconflictingana makine adları</span><span class="sxs-lookup"><span data-stu-id="22491-121">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="22491-122">Çakışan konak adlarını yoksay seçeneği</span><span class="sxs-lookup"><span data-stu-id="22491-122">Ignore Conflicting HostNames Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22491-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="22491-123">-Name</span></span>
<span data-ttu-id="22491-124">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="22491-124">WebApp Name</span></span>

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

### <span data-ttu-id="22491-125">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="22491-125">-Overwrite</span></span>
<span data-ttu-id="22491-126">Overwrite seçeneği</span><span class="sxs-lookup"><span data-stu-id="22491-126">Overwrite Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22491-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22491-127">-ResourceGroupName</span></span>
<span data-ttu-id="22491-128">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="22491-128">Resource Group Name</span></span>

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

### <span data-ttu-id="22491-129">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="22491-129">-Slot</span></span>
<span data-ttu-id="22491-130">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="22491-130">WebApp Slot Name</span></span>

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

### <span data-ttu-id="22491-131">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="22491-131">-StorageAccountUrl</span></span>
<span data-ttu-id="22491-132">Depolama hesabı URL 'Si</span><span class="sxs-lookup"><span data-stu-id="22491-132">Storage Account Url</span></span>

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

### <span data-ttu-id="22491-133">-WebApp</span><span class="sxs-lookup"><span data-stu-id="22491-133">-WebApp</span></span>
<span data-ttu-id="22491-134">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="22491-134">WebApp Object</span></span>

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

### <span data-ttu-id="22491-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22491-135">CommonParameters</span></span>
<span data-ttu-id="22491-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="22491-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22491-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22491-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22491-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="22491-138">INPUTS</span></span>

### <span data-ttu-id="22491-139">System. String</span><span class="sxs-lookup"><span data-stu-id="22491-139">System.String</span></span>

### <span data-ttu-id="22491-140">Microsoft. Azure. Management. Web sitesi. modeller. DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="22491-140">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

### <span data-ttu-id="22491-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="22491-141">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="22491-142">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="22491-142">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="22491-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="22491-143">OUTPUTS</span></span>

### <span data-ttu-id="22491-144">System. void</span><span class="sxs-lookup"><span data-stu-id="22491-144">System.Void</span></span>

## <span data-ttu-id="22491-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="22491-145">NOTES</span></span>

## <span data-ttu-id="22491-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="22491-146">RELATED LINKS</span></span>
