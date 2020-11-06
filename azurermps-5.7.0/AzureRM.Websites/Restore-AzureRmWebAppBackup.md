---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
ms.openlocfilehash: c68d9afb7c9498bbf734abcc376e6f123ebb8ac3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592842"
---
# <span data-ttu-id="7f2de-101">Restore-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="7f2de-101">Restore-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="7f2de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f2de-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f2de-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7f2de-103">SYNTAX</span></span>

### <span data-ttu-id="7f2de-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="7f2de-104">FromResourceName</span></span>
```
Restore-AzureRmWebAppBackup [-Databases <DatabaseBackupSetting[]>] [-IgnoreConflictingHostNames]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

### <span data-ttu-id="7f2de-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="7f2de-105">FromWebApp</span></span>
```
Restore-AzureRmWebAppBackup [-Databases <DatabaseBackupSetting[]>] [-IgnoreConflictingHostNames]
 [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String>
 [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="7f2de-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="7f2de-106">DESCRIPTION</span></span>
<span data-ttu-id="7f2de-107">**Restore-AzureRmWebAppBackup** cmdlet 'ı Azure Web App yedeklemesini geri yükler.</span><span class="sxs-lookup"><span data-stu-id="7f2de-107">The **Restore-AzureRmWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="7f2de-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7f2de-108">EXAMPLES</span></span>

### <span data-ttu-id="7f2de-109">2</span><span class="sxs-lookup"><span data-stu-id="7f2de-109">1:</span></span>
```
PS C:\> Restore-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="7f2de-110">Belirtilen uygulamanın bir yedeğini geri yükler kaynak grubu içinde varsayılan-Web-WestUS https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="7f2de-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="7f2de-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7f2de-111">PARAMETERS</span></span>

### <span data-ttu-id="7f2de-112">-BlobName</span><span class="sxs-lookup"><span data-stu-id="7f2de-112">-BlobName</span></span>
<span data-ttu-id="7f2de-113">Blob adı</span><span class="sxs-lookup"><span data-stu-id="7f2de-113">Blob Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f2de-114">-Veritabanları</span><span class="sxs-lookup"><span data-stu-id="7f2de-114">-Databases</span></span>
<span data-ttu-id="7f2de-115">DatabaseBackupSetting [] türündeki veritabanları</span><span class="sxs-lookup"><span data-stu-id="7f2de-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="7f2de-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f2de-116">-DefaultProfile</span></span>
<span data-ttu-id="7f2de-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7f2de-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f2de-118">-Ignoreconflictingana makine adları</span><span class="sxs-lookup"><span data-stu-id="7f2de-118">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="7f2de-119">Çakışan konak adlarını yoksay seçeneği</span><span class="sxs-lookup"><span data-stu-id="7f2de-119">Ignore Conflicting HostNames Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f2de-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="7f2de-120">-Name</span></span>
<span data-ttu-id="7f2de-121">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="7f2de-121">WebApp Name</span></span>

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

### <span data-ttu-id="7f2de-122">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="7f2de-122">-Overwrite</span></span>
<span data-ttu-id="7f2de-123">Overwrite seçeneği</span><span class="sxs-lookup"><span data-stu-id="7f2de-123">Overwrite Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f2de-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f2de-124">-ResourceGroupName</span></span>
<span data-ttu-id="7f2de-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="7f2de-125">Resource Group Name</span></span>

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

### <span data-ttu-id="7f2de-126">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="7f2de-126">-Slot</span></span>
<span data-ttu-id="7f2de-127">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="7f2de-127">WebApp Slot Name</span></span>

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

### <span data-ttu-id="7f2de-128">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="7f2de-128">-StorageAccountUrl</span></span>
<span data-ttu-id="7f2de-129">Depolama hesabı URL 'Si</span><span class="sxs-lookup"><span data-stu-id="7f2de-129">Storage Account Url</span></span>

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

### <span data-ttu-id="7f2de-130">-WebApp</span><span class="sxs-lookup"><span data-stu-id="7f2de-130">-WebApp</span></span>
<span data-ttu-id="7f2de-131">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="7f2de-131">WebApp Object</span></span>

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

### <span data-ttu-id="7f2de-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f2de-132">CommonParameters</span></span>
<span data-ttu-id="7f2de-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7f2de-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f2de-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f2de-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f2de-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7f2de-135">INPUTS</span></span>

### <span data-ttu-id="7f2de-136">Bölge</span><span class="sxs-lookup"><span data-stu-id="7f2de-136">Site</span></span>
<span data-ttu-id="7f2de-137">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="7f2de-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="7f2de-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7f2de-138">OUTPUTS</span></span>

## <span data-ttu-id="7f2de-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7f2de-139">NOTES</span></span>

## <span data-ttu-id="7f2de-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7f2de-140">RELATED LINKS</span></span>

