---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppBackup.md
ms.openlocfilehash: a4cdec386269bbda7ceb34ec8731c51d7eb1fc44
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593598"
---
# <span data-ttu-id="14c26-101">New-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="14c26-101">New-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="14c26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14c26-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14c26-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="14c26-103">SYNTAX</span></span>

### <span data-ttu-id="14c26-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="14c26-104">FromResourceName</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="14c26-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="14c26-105">FromWebApp</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="14c26-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="14c26-106">DESCRIPTION</span></span>
<span data-ttu-id="14c26-107">**Yeni-AzureRmWebAppBackup** cmdlet 'ı Azure Web App yedeklemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="14c26-107">The **New-AzureRmWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="14c26-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="14c26-108">EXAMPLES</span></span>

### <span data-ttu-id="14c26-109">2</span><span class="sxs-lookup"><span data-stu-id="14c26-109">1:</span></span>
```
PS C:\> New-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="14c26-110">Belirtilen uygulama ContosoWebApp 'nin kaynak grubu içinde varsayılan https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="14c26-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="14c26-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="14c26-111">PARAMETERS</span></span>

### <span data-ttu-id="14c26-112">-BackupName</span><span class="sxs-lookup"><span data-stu-id="14c26-112">-BackupName</span></span>
<span data-ttu-id="14c26-113">Yedek adı</span><span class="sxs-lookup"><span data-stu-id="14c26-113">Backup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14c26-114">-Veritabanları</span><span class="sxs-lookup"><span data-stu-id="14c26-114">-Databases</span></span>
<span data-ttu-id="14c26-115">DatabaseBackupSetting [] türündeki veritabanları</span><span class="sxs-lookup"><span data-stu-id="14c26-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="14c26-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14c26-116">-DefaultProfile</span></span>
<span data-ttu-id="14c26-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="14c26-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14c26-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="14c26-118">-Name</span></span>
<span data-ttu-id="14c26-119">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="14c26-119">WebApp Name</span></span>

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

### <span data-ttu-id="14c26-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14c26-120">-ResourceGroupName</span></span>
<span data-ttu-id="14c26-121">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="14c26-121">Resource Group Name</span></span>

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

### <span data-ttu-id="14c26-122">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="14c26-122">-Slot</span></span>
<span data-ttu-id="14c26-123">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="14c26-123">WebApp Slot Name</span></span>

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

### <span data-ttu-id="14c26-124">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="14c26-124">-StorageAccountUrl</span></span>
<span data-ttu-id="14c26-125">Depolama hesabı URL 'Si</span><span class="sxs-lookup"><span data-stu-id="14c26-125">Storage Account Url</span></span>

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

### <span data-ttu-id="14c26-126">-WebApp</span><span class="sxs-lookup"><span data-stu-id="14c26-126">-WebApp</span></span>
<span data-ttu-id="14c26-127">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="14c26-127">WebApp Object</span></span>

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

### <span data-ttu-id="14c26-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14c26-128">CommonParameters</span></span>
<span data-ttu-id="14c26-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="14c26-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14c26-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14c26-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14c26-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="14c26-131">INPUTS</span></span>

### <span data-ttu-id="14c26-132">System. String</span><span class="sxs-lookup"><span data-stu-id="14c26-132">System.String</span></span>

### <span data-ttu-id="14c26-133">Microsoft. Azure. Management. Web sitesi. modeller. site</span><span class="sxs-lookup"><span data-stu-id="14c26-133">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="14c26-134">Parametreler: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="14c26-134">Parameters: WebApp (ByValue)</span></span>

### <span data-ttu-id="14c26-135">Microsoft. Azure. Management. Web sitesi. modeller. DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="14c26-135">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

## <span data-ttu-id="14c26-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="14c26-136">OUTPUTS</span></span>

### <span data-ttu-id="14c26-137">Microsoft. Azure. Commands. WebApps. cmdlet. WebApps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="14c26-137">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="14c26-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="14c26-138">NOTES</span></span>

## <span data-ttu-id="14c26-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="14c26-139">RELATED LINKS</span></span>
