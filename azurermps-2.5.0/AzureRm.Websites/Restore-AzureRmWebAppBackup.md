---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappbackup
schema: 2.0.0
ms.openlocfilehash: 9c28d9235eefe6c4f33537115b548137c5bc6c88
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939824"
---
# <span data-ttu-id="1f474-101">Restore-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="1f474-101">Restore-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="1f474-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f474-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f474-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1f474-103">SYNTAX</span></span>

### <span data-ttu-id="1f474-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="1f474-104">FromResourceName</span></span>
```
Restore-AzureRmWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite]
 [<CommonParameters>]
```

### <span data-ttu-id="1f474-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="1f474-105">FromWebApp</span></span>
```
Restore-AzureRmWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="1f474-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="1f474-106">DESCRIPTION</span></span>
<span data-ttu-id="1f474-107">**Restore-AzureRmWebAppBackup** cmdlet 'ı Azure Web App yedeklemesini geri yükler.</span><span class="sxs-lookup"><span data-stu-id="1f474-107">The **Restore-AzureRmWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="1f474-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1f474-108">EXAMPLES</span></span>

### <span data-ttu-id="1f474-109">2</span><span class="sxs-lookup"><span data-stu-id="1f474-109">1:</span></span>
```
PS C:\> Restore-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="1f474-110">Belirtilen uygulamanın bir yedeğini geri yükler kaynak grubu içinde varsayılan-Web-WestUS https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="1f474-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="1f474-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1f474-111">PARAMETERS</span></span>

### <span data-ttu-id="1f474-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1f474-112">-AppServicePlan</span></span>
<span data-ttu-id="1f474-113">Geri yüklenen uygulama için App Service planının adı.</span><span class="sxs-lookup"><span data-stu-id="1f474-113">The name of the App Service Plan for the restored app.</span></span> <span data-ttu-id="1f474-114">Boş bırakılırsa uygulamanın geçerli App Service planı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1f474-114">If left empty, the app's current App Service Plan is used.</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f474-115">-BlobName</span><span class="sxs-lookup"><span data-stu-id="1f474-115">-BlobName</span></span>
<span data-ttu-id="1f474-116">Blob adı</span><span class="sxs-lookup"><span data-stu-id="1f474-116">Blob Name</span></span>

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

### <span data-ttu-id="1f474-117">-Veritabanları</span><span class="sxs-lookup"><span data-stu-id="1f474-117">-Databases</span></span>
<span data-ttu-id="1f474-118">DatabaseBackupSetting [] türündeki veritabanları</span><span class="sxs-lookup"><span data-stu-id="1f474-118">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="1f474-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f474-119">-DefaultProfile</span></span>
<span data-ttu-id="1f474-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1f474-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f474-121">-Ignoreconflictingana makine adları</span><span class="sxs-lookup"><span data-stu-id="1f474-121">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="1f474-122">Çakışan konak adlarını yoksay seçeneği</span><span class="sxs-lookup"><span data-stu-id="1f474-122">Ignore Conflicting HostNames Option</span></span>

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

### <span data-ttu-id="1f474-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="1f474-123">-Name</span></span>
<span data-ttu-id="1f474-124">WebApp adı</span><span class="sxs-lookup"><span data-stu-id="1f474-124">WebApp Name</span></span>

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

### <span data-ttu-id="1f474-125">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="1f474-125">-Overwrite</span></span>
<span data-ttu-id="1f474-126">Overwrite seçeneği</span><span class="sxs-lookup"><span data-stu-id="1f474-126">Overwrite Option</span></span>

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

### <span data-ttu-id="1f474-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f474-127">-ResourceGroupName</span></span>
<span data-ttu-id="1f474-128">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="1f474-128">Resource Group Name</span></span>

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

### <span data-ttu-id="1f474-129">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="1f474-129">-Slot</span></span>
<span data-ttu-id="1f474-130">WebApp yuva adı</span><span class="sxs-lookup"><span data-stu-id="1f474-130">WebApp Slot Name</span></span>

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

### <span data-ttu-id="1f474-131">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="1f474-131">-StorageAccountUrl</span></span>
<span data-ttu-id="1f474-132">Depolama hesabı URL 'Si</span><span class="sxs-lookup"><span data-stu-id="1f474-132">Storage Account Url</span></span>

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

### <span data-ttu-id="1f474-133">-WebApp</span><span class="sxs-lookup"><span data-stu-id="1f474-133">-WebApp</span></span>
<span data-ttu-id="1f474-134">WebApp nesnesi</span><span class="sxs-lookup"><span data-stu-id="1f474-134">WebApp Object</span></span>

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

### <span data-ttu-id="1f474-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f474-135">CommonParameters</span></span>
<span data-ttu-id="1f474-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1f474-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f474-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f474-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f474-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1f474-138">INPUTS</span></span>

### <span data-ttu-id="1f474-139">Bölge</span><span class="sxs-lookup"><span data-stu-id="1f474-139">Site</span></span>
<span data-ttu-id="1f474-140">' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="1f474-140">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="1f474-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1f474-141">OUTPUTS</span></span>

## <span data-ttu-id="1f474-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1f474-142">NOTES</span></span>

## <span data-ttu-id="1f474-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1f474-143">RELATED LINKS</span></span>

