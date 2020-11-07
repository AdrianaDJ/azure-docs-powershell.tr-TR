---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppBackup.md
ms.openlocfilehash: 2ef015c3f793dd4636632f17568feb9aaf1b5ad2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753811"
---
# <span data-ttu-id="d9203-101">New-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="d9203-101">New-AzWebAppBackup</span></span>

## <span data-ttu-id="d9203-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9203-102">SYNOPSIS</span></span>

## <span data-ttu-id="d9203-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d9203-103">SYNTAX</span></span>

### <span data-ttu-id="d9203-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="d9203-104">FromResourceName</span></span>
```
New-AzWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="d9203-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="d9203-105">FromWebApp</span></span>
```
New-AzWebAppBackup [[-BackupName] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="d9203-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="d9203-106">DESCRIPTION</span></span>
<span data-ttu-id="d9203-107">**Yeni-AzWebAppBackup** cmdlet 'ı Azure Web App yedeklemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d9203-107">The **New-AzWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="d9203-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d9203-108">EXAMPLES</span></span>

### <span data-ttu-id="d9203-109">2</span><span class="sxs-lookup"><span data-stu-id="d9203-109">1:</span></span>
```
PS C:\> New-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="d9203-110">Belirtilen uygulama ContosoWebApp 'nin kaynak grubu içinde varsayılan https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="d9203-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="d9203-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d9203-111">PARAMETERS</span></span>

### <span data-ttu-id="d9203-112">-BackupName</span><span class="sxs-lookup"><span data-stu-id="d9203-112">-BackupName</span></span>
<span data-ttu-id="d9203-113">Yedek adı</span><span class="sxs-lookup"><span data-stu-id="d9203-113">Backup Name</span></span>

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

### <span data-ttu-id="d9203-114">-Veritabanları</span><span class="sxs-lookup"><span data-stu-id="d9203-114">-Databases</span></span>
<span data-ttu-id="d9203-115">DatabaseBackupSetting [] türündeki veritabanları</span><span class="sxs-lookup"><span data-stu-id="d9203-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="d9203-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9203-116">-DefaultProfile</span></span>
<span data-ttu-id="d9203-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d9203-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9203-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="d9203-118">-Name</span></span>
<span data-ttu-id="d9203-119">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="d9203-119">WebApp Name</span></span>

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

### <span data-ttu-id="d9203-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9203-120">-ResourceGroupName</span></span>
<span data-ttu-id="d9203-121">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="d9203-121">Resource Group Name</span></span>

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

### <span data-ttu-id="d9203-122">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="d9203-122">-Slot</span></span>
<span data-ttu-id="d9203-123">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="d9203-123">WebApp Slot Name</span></span>

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

### <span data-ttu-id="d9203-124">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="d9203-124">-StorageAccountUrl</span></span>
<span data-ttu-id="d9203-125">Depolama hesabı URL 'Si</span><span class="sxs-lookup"><span data-stu-id="d9203-125">Storage Account Url</span></span>

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

### <span data-ttu-id="d9203-126">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d9203-126">-WebApp</span></span>
<span data-ttu-id="d9203-127">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="d9203-127">WebApp Object</span></span>

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

### <span data-ttu-id="d9203-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9203-128">CommonParameters</span></span>
<span data-ttu-id="d9203-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d9203-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9203-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9203-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9203-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d9203-131">INPUTS</span></span>

### <span data-ttu-id="d9203-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d9203-132">System.String</span></span>

### <span data-ttu-id="d9203-133">Microsoft. Azure. Commands. WebApps. modeller. PSSite</span><span class="sxs-lookup"><span data-stu-id="d9203-133">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="d9203-134">Microsoft. Azure. Management. Web sitesi. modeller. DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="d9203-134">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

## <span data-ttu-id="d9203-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d9203-135">OUTPUTS</span></span>

### <span data-ttu-id="d9203-136">Microsoft. Azure. Commands. WebApps. cmdlet. WebApps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="d9203-136">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="d9203-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d9203-137">NOTES</span></span>

## <span data-ttu-id="d9203-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d9203-138">RELATED LINKS</span></span>
