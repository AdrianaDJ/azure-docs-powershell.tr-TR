---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
ms.openlocfilehash: efb570c22b5345b9d75fdf96dca061dc5cf7847f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590774"
---
# <span data-ttu-id="55d91-101">Restore-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="55d91-101">Restore-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="55d91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55d91-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55d91-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="55d91-103">SYNTAX</span></span>

### <span data-ttu-id="55d91-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="55d91-104">FromResourceName</span></span>
```
Restore-AzureRmWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite]
 [<CommonParameters>]
```

### <span data-ttu-id="55d91-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="55d91-105">FromWebApp</span></span>
```
Restore-AzureRmWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="55d91-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="55d91-106">DESCRIPTION</span></span>
<span data-ttu-id="55d91-107">**Restore-AzureRmWebAppBackup** cmdlet 'ı Azure Web App yedeklemesini geri yükler.</span><span class="sxs-lookup"><span data-stu-id="55d91-107">The **Restore-AzureRmWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="55d91-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="55d91-108">EXAMPLES</span></span>

### <span data-ttu-id="55d91-109">2</span><span class="sxs-lookup"><span data-stu-id="55d91-109">1:</span></span>
```
PS C:\> Restore-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="55d91-110">Belirtilen uygulamanın bir yedeğini geri yükler kaynak grubu içinde varsayılan-Web-WestUS https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="55d91-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="55d91-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="55d91-111">PARAMETERS</span></span>

### <span data-ttu-id="55d91-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="55d91-112">-AppServicePlan</span></span>
<span data-ttu-id="55d91-113">Geri yüklenen uygulama için App Service planının adı.</span><span class="sxs-lookup"><span data-stu-id="55d91-113">The name of the App Service Plan for the restored app.</span></span> <span data-ttu-id="55d91-114">Boş bırakılırsa uygulamanın geçerli App Service planı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="55d91-114">If left empty, the app's current App Service Plan is used.</span></span>

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

### <span data-ttu-id="55d91-115">-BlobName</span><span class="sxs-lookup"><span data-stu-id="55d91-115">-BlobName</span></span>
<span data-ttu-id="55d91-116">Blob adı</span><span class="sxs-lookup"><span data-stu-id="55d91-116">Blob Name</span></span>

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

### <span data-ttu-id="55d91-117">-Veritabanları</span><span class="sxs-lookup"><span data-stu-id="55d91-117">-Databases</span></span>
<span data-ttu-id="55d91-118">DatabaseBackupSetting [] türündeki veritabanları</span><span class="sxs-lookup"><span data-stu-id="55d91-118">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="55d91-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55d91-119">-DefaultProfile</span></span>
<span data-ttu-id="55d91-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="55d91-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55d91-121">-Ignoreconflictingana makine adları</span><span class="sxs-lookup"><span data-stu-id="55d91-121">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="55d91-122">Çakışan konak adlarını yoksay seçeneği</span><span class="sxs-lookup"><span data-stu-id="55d91-122">Ignore Conflicting HostNames Option</span></span>

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

### <span data-ttu-id="55d91-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="55d91-123">-Name</span></span>
<span data-ttu-id="55d91-124">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="55d91-124">WebApp Name</span></span>

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

### <span data-ttu-id="55d91-125">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="55d91-125">-Overwrite</span></span>
<span data-ttu-id="55d91-126">Overwrite seçeneği</span><span class="sxs-lookup"><span data-stu-id="55d91-126">Overwrite Option</span></span>

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

### <span data-ttu-id="55d91-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55d91-127">-ResourceGroupName</span></span>
<span data-ttu-id="55d91-128">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="55d91-128">Resource Group Name</span></span>

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

### <span data-ttu-id="55d91-129">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="55d91-129">-Slot</span></span>
<span data-ttu-id="55d91-130">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="55d91-130">WebApp Slot Name</span></span>

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

### <span data-ttu-id="55d91-131">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="55d91-131">-StorageAccountUrl</span></span>
<span data-ttu-id="55d91-132">Depolama hesabı URL 'Si</span><span class="sxs-lookup"><span data-stu-id="55d91-132">Storage Account Url</span></span>

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

### <span data-ttu-id="55d91-133">-WebApp</span><span class="sxs-lookup"><span data-stu-id="55d91-133">-WebApp</span></span>
<span data-ttu-id="55d91-134">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="55d91-134">WebApp Object</span></span>

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

### <span data-ttu-id="55d91-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55d91-135">CommonParameters</span></span>
<span data-ttu-id="55d91-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="55d91-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55d91-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55d91-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55d91-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="55d91-138">INPUTS</span></span>

### <span data-ttu-id="55d91-139">System. String</span><span class="sxs-lookup"><span data-stu-id="55d91-139">System.String</span></span>

### <span data-ttu-id="55d91-140">Microsoft. Azure. Management. Web sitesi. modeller. DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="55d91-140">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

### <span data-ttu-id="55d91-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="55d91-141">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="55d91-142">Microsoft. Azure. Management. Web sitesi. modeller. site</span><span class="sxs-lookup"><span data-stu-id="55d91-142">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="55d91-143">Parametreler: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="55d91-143">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="55d91-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="55d91-144">OUTPUTS</span></span>

### <span data-ttu-id="55d91-145">System. void</span><span class="sxs-lookup"><span data-stu-id="55d91-145">System.Void</span></span>

## <span data-ttu-id="55d91-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="55d91-146">NOTES</span></span>

## <span data-ttu-id="55d91-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="55d91-147">RELATED LINKS</span></span>
