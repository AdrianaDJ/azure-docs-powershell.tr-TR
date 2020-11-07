---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppBackup.md
ms.openlocfilehash: 03c9b54dd83f4689f763ef45e0f9a7c0d8b89672
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764747"
---
# <span data-ttu-id="0ee70-101">New-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="0ee70-101">New-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="0ee70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ee70-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ee70-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0ee70-103">SYNTAX</span></span>

### <span data-ttu-id="0ee70-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="0ee70-104">FromResourceName</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="0ee70-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="0ee70-105">FromWebApp</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="0ee70-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="0ee70-106">DESCRIPTION</span></span>
<span data-ttu-id="0ee70-107">**Yeni-AzureRmWebAppBackup** cmdlet 'ı Azure Web App yedeklemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0ee70-107">The **New-AzureRmWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="0ee70-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0ee70-108">EXAMPLES</span></span>

### <span data-ttu-id="0ee70-109">2</span><span class="sxs-lookup"><span data-stu-id="0ee70-109">1:</span></span>
```
PS C:\> New-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="0ee70-110">Belirtilen uygulama ContosoWebApp 'nin kaynak grubu içinde varsayılan https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="0ee70-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="0ee70-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0ee70-111">PARAMETERS</span></span>

### <span data-ttu-id="0ee70-112">-BackupName</span><span class="sxs-lookup"><span data-stu-id="0ee70-112">-BackupName</span></span>
<span data-ttu-id="0ee70-113">Yedek adı</span><span class="sxs-lookup"><span data-stu-id="0ee70-113">Backup Name</span></span>

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

### <span data-ttu-id="0ee70-114">-Veritabanları</span><span class="sxs-lookup"><span data-stu-id="0ee70-114">-Databases</span></span>
<span data-ttu-id="0ee70-115">DatabaseBackupSetting [] türündeki veritabanları</span><span class="sxs-lookup"><span data-stu-id="0ee70-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="0ee70-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="0ee70-116">-Name</span></span>
<span data-ttu-id="0ee70-117">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="0ee70-117">WebApp Name</span></span>

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

### <span data-ttu-id="0ee70-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ee70-118">-ResourceGroupName</span></span>
<span data-ttu-id="0ee70-119">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="0ee70-119">Resource Group Name</span></span>

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

### <span data-ttu-id="0ee70-120">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="0ee70-120">-Slot</span></span>
<span data-ttu-id="0ee70-121">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="0ee70-121">WebApp Slot Name</span></span>

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

### <span data-ttu-id="0ee70-122">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="0ee70-122">-StorageAccountUrl</span></span>
<span data-ttu-id="0ee70-123">Depolama hesabı URL 'Si</span><span class="sxs-lookup"><span data-stu-id="0ee70-123">Storage Account Url</span></span>

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

### <span data-ttu-id="0ee70-124">-WebApp</span><span class="sxs-lookup"><span data-stu-id="0ee70-124">-WebApp</span></span>
<span data-ttu-id="0ee70-125">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="0ee70-125">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ee70-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ee70-126">-DefaultProfile</span></span>
<span data-ttu-id="0ee70-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0ee70-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ee70-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ee70-128">CommonParameters</span></span>
<span data-ttu-id="0ee70-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0ee70-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ee70-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ee70-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ee70-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0ee70-131">INPUTS</span></span>

### <span data-ttu-id="0ee70-132">Bölge</span><span class="sxs-lookup"><span data-stu-id="0ee70-132">Site</span></span>
<span data-ttu-id="0ee70-133">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="0ee70-133">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="0ee70-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0ee70-134">OUTPUTS</span></span>

### <span data-ttu-id="0ee70-135">Microsoft. Azure. Commands. WebApps. cmdlet. WebApps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="0ee70-135">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="0ee70-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0ee70-136">NOTES</span></span>

## <span data-ttu-id="0ee70-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0ee70-137">RELATED LINKS</span></span>

