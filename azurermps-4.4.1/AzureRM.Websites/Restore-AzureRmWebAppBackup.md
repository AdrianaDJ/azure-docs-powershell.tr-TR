---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
ms.openlocfilehash: 07cf4daffeaf00c516bc5b179e5f4a2133a2c4ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586865"
---
# <span data-ttu-id="8f85d-101">Restore-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="8f85d-101">Restore-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="8f85d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f85d-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f85d-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8f85d-103">SYNTAX</span></span>

### <span data-ttu-id="8f85d-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="8f85d-104">FromResourceName</span></span>
```
Restore-AzureRmWebAppBackup [-Databases <DatabaseBackupSetting[]>] [-IgnoreConflictingHostNames]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

### <span data-ttu-id="8f85d-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="8f85d-105">FromWebApp</span></span>
```
Restore-AzureRmWebAppBackup [-Databases <DatabaseBackupSetting[]>] [-IgnoreConflictingHostNames]
 [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String>
 [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="8f85d-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="8f85d-106">DESCRIPTION</span></span>
<span data-ttu-id="8f85d-107">**Restore-AzureRmWebAppBackup** cmdlet 'ı Azure Web App yedeklemesini geri yükler.</span><span class="sxs-lookup"><span data-stu-id="8f85d-107">The **Restore-AzureRmWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="8f85d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8f85d-108">EXAMPLES</span></span>

### <span data-ttu-id="8f85d-109">2</span><span class="sxs-lookup"><span data-stu-id="8f85d-109">1:</span></span>
```
PS C:\> Restore-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="8f85d-110">Belirtilen uygulamanın bir yedeğini geri yükler kaynak grubu içinde varsayılan-Web-WestUS https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="8f85d-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="8f85d-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8f85d-111">PARAMETERS</span></span>

### <span data-ttu-id="8f85d-112">-BlobName</span><span class="sxs-lookup"><span data-stu-id="8f85d-112">-BlobName</span></span>
<span data-ttu-id="8f85d-113">Blob adı</span><span class="sxs-lookup"><span data-stu-id="8f85d-113">Blob Name</span></span>

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

### <span data-ttu-id="8f85d-114">-Veritabanları</span><span class="sxs-lookup"><span data-stu-id="8f85d-114">-Databases</span></span>
<span data-ttu-id="8f85d-115">DatabaseBackupSetting [] türündeki veritabanları</span><span class="sxs-lookup"><span data-stu-id="8f85d-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="8f85d-116">-Ignoreconflictingana makine adları</span><span class="sxs-lookup"><span data-stu-id="8f85d-116">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="8f85d-117">Çakışan konak adlarını yoksay seçeneği</span><span class="sxs-lookup"><span data-stu-id="8f85d-117">Ignore Conflicting HostNames Option</span></span>

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

### <span data-ttu-id="8f85d-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="8f85d-118">-Name</span></span>
<span data-ttu-id="8f85d-119">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="8f85d-119">WebApp Name</span></span>

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

### <span data-ttu-id="8f85d-120">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="8f85d-120">-Overwrite</span></span>
<span data-ttu-id="8f85d-121">Overwrite seçeneği</span><span class="sxs-lookup"><span data-stu-id="8f85d-121">Overwrite Option</span></span>

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

### <span data-ttu-id="8f85d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f85d-122">-ResourceGroupName</span></span>
<span data-ttu-id="8f85d-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="8f85d-123">Resource Group Name</span></span>

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

### <span data-ttu-id="8f85d-124">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="8f85d-124">-Slot</span></span>
<span data-ttu-id="8f85d-125">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="8f85d-125">WebApp Slot Name</span></span>

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

### <span data-ttu-id="8f85d-126">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="8f85d-126">-StorageAccountUrl</span></span>
<span data-ttu-id="8f85d-127">Depolama hesabı URL 'Si</span><span class="sxs-lookup"><span data-stu-id="8f85d-127">Storage Account Url</span></span>

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

### <span data-ttu-id="8f85d-128">-WebApp</span><span class="sxs-lookup"><span data-stu-id="8f85d-128">-WebApp</span></span>
<span data-ttu-id="8f85d-129">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="8f85d-129">WebApp Object</span></span>

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

### <span data-ttu-id="8f85d-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f85d-130">-DefaultProfile</span></span>
<span data-ttu-id="8f85d-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8f85d-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f85d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f85d-132">CommonParameters</span></span>
<span data-ttu-id="8f85d-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8f85d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f85d-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f85d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f85d-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8f85d-135">INPUTS</span></span>

### <span data-ttu-id="8f85d-136">Bölge</span><span class="sxs-lookup"><span data-stu-id="8f85d-136">Site</span></span>
<span data-ttu-id="8f85d-137">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="8f85d-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="8f85d-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8f85d-138">OUTPUTS</span></span>

## <span data-ttu-id="8f85d-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8f85d-139">NOTES</span></span>

## <span data-ttu-id="8f85d-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8f85d-140">RELATED LINKS</span></span>

