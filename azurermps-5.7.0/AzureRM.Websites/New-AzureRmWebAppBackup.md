---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppBackup.md
ms.openlocfilehash: 7784ea832faef9f73b46b04d6ad36bebe0e2f36d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592365"
---
# <span data-ttu-id="f504d-101">New-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="f504d-101">New-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="f504d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f504d-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f504d-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f504d-103">SYNTAX</span></span>

### <span data-ttu-id="f504d-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="f504d-104">FromResourceName</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="f504d-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="f504d-105">FromWebApp</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="f504d-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="f504d-106">DESCRIPTION</span></span>
<span data-ttu-id="f504d-107">**Yeni-AzureRmWebAppBackup** cmdlet 'ı Azure Web App yedeklemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f504d-107">The **New-AzureRmWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="f504d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f504d-108">EXAMPLES</span></span>

### <span data-ttu-id="f504d-109">2</span><span class="sxs-lookup"><span data-stu-id="f504d-109">1:</span></span>
```
PS C:\> New-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="f504d-110">Belirtilen uygulama ContosoWebApp 'nin kaynak grubu içinde varsayılan https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="f504d-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="f504d-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f504d-111">PARAMETERS</span></span>

### <span data-ttu-id="f504d-112">-BackupName</span><span class="sxs-lookup"><span data-stu-id="f504d-112">-BackupName</span></span>
<span data-ttu-id="f504d-113">Yedek adı</span><span class="sxs-lookup"><span data-stu-id="f504d-113">Backup Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f504d-114">-Veritabanları</span><span class="sxs-lookup"><span data-stu-id="f504d-114">-Databases</span></span>
<span data-ttu-id="f504d-115">DatabaseBackupSetting [] türündeki veritabanları</span><span class="sxs-lookup"><span data-stu-id="f504d-115">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f504d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f504d-116">-DefaultProfile</span></span>
<span data-ttu-id="f504d-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f504d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f504d-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="f504d-118">-Name</span></span>
<span data-ttu-id="f504d-119">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="f504d-119">WebApp Name</span></span>

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

### <span data-ttu-id="f504d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f504d-120">-ResourceGroupName</span></span>
<span data-ttu-id="f504d-121">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="f504d-121">Resource Group Name</span></span>

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

### <span data-ttu-id="f504d-122">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="f504d-122">-Slot</span></span>
<span data-ttu-id="f504d-123">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="f504d-123">WebApp Slot Name</span></span>

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

### <span data-ttu-id="f504d-124">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="f504d-124">-StorageAccountUrl</span></span>
<span data-ttu-id="f504d-125">Depolama hesabı URL 'Si</span><span class="sxs-lookup"><span data-stu-id="f504d-125">Storage Account Url</span></span>

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

### <span data-ttu-id="f504d-126">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f504d-126">-WebApp</span></span>
<span data-ttu-id="f504d-127">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="f504d-127">WebApp Object</span></span>

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

### <span data-ttu-id="f504d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f504d-128">CommonParameters</span></span>
<span data-ttu-id="f504d-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f504d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f504d-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f504d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f504d-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f504d-131">INPUTS</span></span>

### <span data-ttu-id="f504d-132">Bölge</span><span class="sxs-lookup"><span data-stu-id="f504d-132">Site</span></span>
<span data-ttu-id="f504d-133">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="f504d-133">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f504d-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f504d-134">OUTPUTS</span></span>

### <span data-ttu-id="f504d-135">Microsoft. Azure. Commands. WebApps. cmdlet. WebApps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="f504d-135">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="f504d-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f504d-136">NOTES</span></span>

## <span data-ttu-id="f504d-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f504d-137">RELATED LINKS</span></span>

