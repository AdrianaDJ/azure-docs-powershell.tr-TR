---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 35588231-CBAC-4411-9531-9A06BD298ACA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7fdcad4b3a0f41f0589e49d4b33a767b93267855
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105548"
---
# <span data-ttu-id="556e4-101">Get-AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="556e4-101">Get-AzureStorageKey</span></span>

## <span data-ttu-id="556e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="556e4-102">SYNOPSIS</span></span>
<span data-ttu-id="556e4-103">Azure depolama hesabı için birincil ve ikincil depolama hesabı anahtarlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="556e4-103">Returns the primary and secondary storage account keys for an Azure storage account.</span></span>

## <span data-ttu-id="556e4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="556e4-104">SYNTAX</span></span>

```
Get-AzureStorageKey [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="556e4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="556e4-105">DESCRIPTION</span></span>
<span data-ttu-id="556e4-106">**Get-AzureStorageKey** cmdlet 'ı, Azure depolama hesabı adı, birincil hesap anahtarı ve belirtilen Azure depolama hesabının ikincil hesap anahtarını özellikler olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="556e4-106">The **Get-AzureStorageKey** cmdlet returns an object with the Azure Storage account name, the primary account key, and the secondary account key of the specified Azure storage account as properties.</span></span>

## <span data-ttu-id="556e4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="556e4-107">EXAMPLES</span></span>

### <span data-ttu-id="556e4-108">Örnek 1: birincil ve ikincil depolama anahtarlarını içeren bir nesne alma</span><span class="sxs-lookup"><span data-stu-id="556e4-108">Example 1: Get an object that contains primary and secondary storage keys</span></span>
```
PS C:\> Get-AzureStorageKey -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="556e4-109">Bu komut, ContosoStore01 depolama hesabı için birincil ve ikincil depolama anahtarlarına sahip bir nesne alır.</span><span class="sxs-lookup"><span data-stu-id="556e4-109">This command gets an object with the primary and secondary storage keys for the ContosoStore01 storage account.</span></span>

### <span data-ttu-id="556e4-110">Örnek 2: birincil depolama hesabı anahtarını alma ve bir değişkende depolama</span><span class="sxs-lookup"><span data-stu-id="556e4-110">Example 2: Get the primary storage account key and store it in a variable</span></span>
```
PS C:\> $ContosoStoreKey = (Get-AzureStorageKey -StorageAccountName "ContosoStore01").Primary
```

<span data-ttu-id="556e4-111">Bu komut, $ContosoStoreKey değişkenine ContosoStore01 depolama hesabı için birincil depolama hesabı anahtarını koyar.</span><span class="sxs-lookup"><span data-stu-id="556e4-111">This command puts the primary storage account key for the ContosoStore01 storage account in the $ContosoStoreKey variable.</span></span>

## <span data-ttu-id="556e4-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="556e4-112">PARAMETERS</span></span>

### <span data-ttu-id="556e4-113">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="556e4-113">-InformationAction</span></span>
<span data-ttu-id="556e4-114">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="556e4-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="556e4-115">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="556e4-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="556e4-116">'A</span><span class="sxs-lookup"><span data-stu-id="556e4-116">Continue</span></span>
- <span data-ttu-id="556e4-117">Manıza</span><span class="sxs-lookup"><span data-stu-id="556e4-117">Ignore</span></span>
- <span data-ttu-id="556e4-118">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="556e4-118">Inquire</span></span>
- <span data-ttu-id="556e4-119">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="556e4-119">SilentlyContinue</span></span>
- <span data-ttu-id="556e4-120">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="556e4-120">Stop</span></span>
- <span data-ttu-id="556e4-121">Biliriz</span><span class="sxs-lookup"><span data-stu-id="556e4-121">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="556e4-122">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="556e4-122">-InformationVariable</span></span>
<span data-ttu-id="556e4-123">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="556e4-123">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="556e4-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="556e4-124">-Profile</span></span>
<span data-ttu-id="556e4-125">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="556e4-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="556e4-126">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="556e4-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="556e4-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="556e4-127">-StorageAccountName</span></span>
<span data-ttu-id="556e4-128">Depolama hesabı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="556e4-128">Specifies the storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="556e4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="556e4-129">CommonParameters</span></span>
<span data-ttu-id="556e4-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="556e4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="556e4-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="556e4-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="556e4-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="556e4-132">INPUTS</span></span>

## <span data-ttu-id="556e4-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="556e4-133">OUTPUTS</span></span>

## <span data-ttu-id="556e4-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="556e4-134">NOTES</span></span>
* <span data-ttu-id="556e4-135">Node.js konusunda yardım almak için `help node-dev` komutu kullanın.</span><span class="sxs-lookup"><span data-stu-id="556e4-135">To get help with Node.js, use the `help node-dev` command.</span></span> <span data-ttu-id="556e4-136">PHP uzantıları ile ilgili yardım için, `help php-dev` komutu kullanın.</span><span class="sxs-lookup"><span data-stu-id="556e4-136">For help with PHP extensions, use the `help php-dev` command.</span></span>

## <span data-ttu-id="556e4-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="556e4-137">RELATED LINKS</span></span>

[<span data-ttu-id="556e4-138">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="556e4-138">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="556e4-139">Yeni-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="556e4-139">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="556e4-140">New-AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="556e4-140">New-AzureStorageKey</span></span>](./New-AzureStorageKey.md)

[<span data-ttu-id="556e4-141">Remove-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="556e4-141">Remove-AzureStorageAccount</span></span>](./Remove-AzureStorageAccount.md)

[<span data-ttu-id="556e4-142">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="556e4-142">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)


