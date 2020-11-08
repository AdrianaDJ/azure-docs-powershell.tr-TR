---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 99A03E14-254E-4E72-8EA9-2FE2A5CEA597
online version: ''
schema: 2.0.0
ms.openlocfilehash: 58e7cafb1fe774abcaf2290168b8254562bad89b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105682"
---
# <span data-ttu-id="85057-101">Enable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="85057-101">Enable-AzureWebsiteApplicationDiagnostic</span></span>

## <span data-ttu-id="85057-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85057-102">SYNOPSIS</span></span>
<span data-ttu-id="85057-103">Azure Web sitesinde uygulama tanılamasını mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="85057-103">Enables application diagnostics on an Azure website.</span></span>

## <span data-ttu-id="85057-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="85057-104">SYNTAX</span></span>

### <span data-ttu-id="85057-105">FileParameterSet</span><span class="sxs-lookup"><span data-stu-id="85057-105">FileParameterSet</span></span>
```
Enable-AzureWebsiteApplicationDiagnostic [-PassThru] [-File] -LogLevel <LogEntryType> [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="85057-106">TableStorageParameterSet</span><span class="sxs-lookup"><span data-stu-id="85057-106">TableStorageParameterSet</span></span>
```
Enable-AzureWebsiteApplicationDiagnostic [-PassThru] [-TableStorage] -LogLevel <LogEntryType>
 [-StorageAccountName <String>] [-StorageTableName <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="85057-107">BlobStorageParameterSet</span><span class="sxs-lookup"><span data-stu-id="85057-107">BlobStorageParameterSet</span></span>
```
Enable-AzureWebsiteApplicationDiagnostic [-PassThru] [-BlobStorage] -LogLevel <LogEntryType>
 [-StorageAccountName <String>] [-StorageBlobContainerName <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="85057-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="85057-108">DESCRIPTION</span></span>
<span data-ttu-id="85057-109">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="85057-109">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="85057-110">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="85057-110">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="85057-111">Bir Azure Web sitesinde Application Diagnostics 'i sağlar ve günlüklerin depolama alanını dosya sisteminde veya Azure Storage 'da yapılandırmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="85057-111">Enables application diagnostics on an Azure website, and allows you to configure storage of logs on a file system or on Azure storage.</span></span>

## <span data-ttu-id="85057-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="85057-112">EXAMPLES</span></span>

### <span data-ttu-id="85057-113">Örnek 1: dosya sistemini kullanarak tanılamayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="85057-113">Example 1: Enable diagnostics using file system</span></span>
```
PS C:\> Enable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -File -LogLevel Verbose
```

<span data-ttu-id="85057-114">Bu örnek, dosya sisteminde ayrıntı düzeyiyle uygulama günlüğünü etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="85057-114">This example enables application logging on file system with verbose level.</span></span>

### <span data-ttu-id="85057-115">Örnek 2: Azure depolama kullanarak günlüğü etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="85057-115">Example 2: Enable logging using Azure Storage</span></span>
```
PS C:\> Enable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -Storage -LogLevel Information -StorageAccountName myaccount
```

<span data-ttu-id="85057-116">Bu örnek, günlük düzeyi olan Hesabım adlı depolama hesabını kullanarak uygulama günlüğünün bilgi ayarlanmasını olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="85057-116">This example enables application logging using storage account named myaccount with logging level set to Information.</span></span>

## <span data-ttu-id="85057-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="85057-117">PARAMETERS</span></span>

### <span data-ttu-id="85057-118">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="85057-118">-BlobStorage</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: BlobStorageParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85057-119">-Dosya</span><span class="sxs-lookup"><span data-stu-id="85057-119">-File</span></span>
<span data-ttu-id="85057-120">Günlük dosyalarını depolamak için bir dosya sistemi kullanmak istediğinizi belirtir.</span><span class="sxs-lookup"><span data-stu-id="85057-120">Specifies that you want to use a file system to store the log files.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FileParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85057-121">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="85057-121">-LogLevel</span></span>
<span data-ttu-id="85057-122">Depolanacak günlük düzeyi.</span><span class="sxs-lookup"><span data-stu-id="85057-122">The log level to store.</span></span>
<span data-ttu-id="85057-123">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="85057-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="85057-124">Hatalar</span><span class="sxs-lookup"><span data-stu-id="85057-124">Error</span></span>
- <span data-ttu-id="85057-125">Uyarılarla</span><span class="sxs-lookup"><span data-stu-id="85057-125">Warning</span></span>
- <span data-ttu-id="85057-126">Bilgisini</span><span class="sxs-lookup"><span data-stu-id="85057-126">Information</span></span>
- <span data-ttu-id="85057-127">Kapsamlı</span><span class="sxs-lookup"><span data-stu-id="85057-127">Verbose</span></span>

```yaml
Type: LogEntryType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85057-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="85057-128">-Name</span></span>
<span data-ttu-id="85057-129">Azure Web sitesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="85057-129">Specifies the name of the Azure website.</span></span>

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

### <span data-ttu-id="85057-130">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="85057-130">-PassThru</span></span>
<span data-ttu-id="85057-131">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="85057-131">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="85057-132">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="85057-132">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85057-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="85057-133">-Profile</span></span>
<span data-ttu-id="85057-134">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="85057-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="85057-135">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="85057-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85057-136">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="85057-136">-Slot</span></span>
<span data-ttu-id="85057-137">Yuvanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="85057-137">Specifies the name of the slot.</span></span>

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

### <span data-ttu-id="85057-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="85057-138">-StorageAccountName</span></span>
<span data-ttu-id="85057-139">Günlükleri depolamak için kullanılacak depolama hesabı.</span><span class="sxs-lookup"><span data-stu-id="85057-139">The storage account to use for storing the logs.</span></span>
<span data-ttu-id="85057-140">Belirtilmemişse CurrentStorageAccount kullanılır.</span><span class="sxs-lookup"><span data-stu-id="85057-140">If not specified, the CurrentStorageAccount is used.</span></span>

```yaml
Type: String
Parameter Sets: TableStorageParameterSet, BlobStorageParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85057-141">-StorageBlobContainerName</span><span class="sxs-lookup"><span data-stu-id="85057-141">-StorageBlobContainerName</span></span>
```yaml
Type: String
Parameter Sets: BlobStorageParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85057-142">-StorageTableName</span><span class="sxs-lookup"><span data-stu-id="85057-142">-StorageTableName</span></span>
```yaml
Type: String
Parameter Sets: TableStorageParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85057-143">-TableStorage</span><span class="sxs-lookup"><span data-stu-id="85057-143">-TableStorage</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: TableStorageParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85057-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85057-144">CommonParameters</span></span>
<span data-ttu-id="85057-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="85057-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85057-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85057-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85057-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="85057-147">INPUTS</span></span>

## <span data-ttu-id="85057-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="85057-148">OUTPUTS</span></span>

## <span data-ttu-id="85057-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="85057-149">NOTES</span></span>

## <span data-ttu-id="85057-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="85057-150">RELATED LINKS</span></span>

[<span data-ttu-id="85057-151">Disable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="85057-151">Disable-AzureWebsiteApplicationDiagnostic</span></span>](./Disable-AzureWebsiteApplicationDiagnostic.md)

[<span data-ttu-id="85057-152">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="85057-152">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="85057-153">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="85057-153">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="85057-154">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="85057-154">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="85057-155">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="85057-155">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


