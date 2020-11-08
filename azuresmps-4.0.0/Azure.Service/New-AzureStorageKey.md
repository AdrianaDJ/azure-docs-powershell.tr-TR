---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 09ABE9E2-1080-4DEF-92DD-B8FF4C8B308C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9afdaafa57592239d0c24870e4459d650fac84c3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106203"
---
# <span data-ttu-id="227d0-101">New-AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="227d0-101">New-AzureStorageKey</span></span>

## <span data-ttu-id="227d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="227d0-102">SYNOPSIS</span></span>
<span data-ttu-id="227d0-103">Azure depolama hesabı için depolama anahtarlarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="227d0-103">Regenerates storage keys for an Azure storage account.</span></span>

## <span data-ttu-id="227d0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="227d0-104">SYNTAX</span></span>

```
New-AzureStorageKey [-KeyType] <String> [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="227d0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="227d0-105">DESCRIPTION</span></span>
<span data-ttu-id="227d0-106">**New-AzureStorageKey** cmdlet 'ı Azure depolama hesabı için birincil veya ikincil anahtarı yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="227d0-106">The **New-AzureStorageKey** cmdlet regenerates the primary or secondary key for an Azure Storage account.</span></span>
<span data-ttu-id="227d0-107">Depolama hesabı adı, birincil anahtar ve ikincil anahtar içeren bir nesneyi özellikler olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="227d0-107">It returns an object that contains the storage account name, primary key, and secondary key as properties.</span></span>

## <span data-ttu-id="227d0-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="227d0-108">EXAMPLES</span></span>

### <span data-ttu-id="227d0-109">Örnek 1: birincil depolama anahtarını yeniden oluşturma</span><span class="sxs-lookup"><span data-stu-id="227d0-109">Example 1: Regenerate a primary storage key</span></span>
```
PS C:\> New-AzureStorageKey -KeyType "Primary" -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="227d0-110">Bu komut, ContosoStore01 depolama hesabı için birincil depolama anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="227d0-110">This command regenerates the primary storage key for the ContosoStore01 storage account.</span></span>

### <span data-ttu-id="227d0-111">Örnek 2: ikincil depolama anahtarını yeniden oluşturma ve bir değişkende kaydetme</span><span class="sxs-lookup"><span data-stu-id="227d0-111">Example 2: Regenerate a secondary storage key and save it in a variable</span></span>
```
PS C:\> $ContosoStoreKey = New-AzureStorageKey -KeyType "Secondary" -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="227d0-112">Bu komut, ContosoStore01 depolama hesabının ikincil depolama anahtarını yeniden oluşturup $ContosoStoreKey güncelleştirilmiş depolama hesabı anahtarı bilgilerini depolar.</span><span class="sxs-lookup"><span data-stu-id="227d0-112">This command regenerate the secondary storage key for the ContosoStore01 storage account and stores the updated storage account key information in the $ContosoStoreKey.</span></span>

## <span data-ttu-id="227d0-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="227d0-113">PARAMETERS</span></span>

### <span data-ttu-id="227d0-114">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="227d0-114">-InformationAction</span></span>
<span data-ttu-id="227d0-115">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="227d0-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="227d0-116">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="227d0-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="227d0-117">'A</span><span class="sxs-lookup"><span data-stu-id="227d0-117">Continue</span></span>
- <span data-ttu-id="227d0-118">Manıza</span><span class="sxs-lookup"><span data-stu-id="227d0-118">Ignore</span></span>
- <span data-ttu-id="227d0-119">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="227d0-119">Inquire</span></span>
- <span data-ttu-id="227d0-120">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="227d0-120">SilentlyContinue</span></span>
- <span data-ttu-id="227d0-121">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="227d0-121">Stop</span></span>
- <span data-ttu-id="227d0-122">Biliriz</span><span class="sxs-lookup"><span data-stu-id="227d0-122">Suspend</span></span>

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

### <span data-ttu-id="227d0-123">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="227d0-123">-InformationVariable</span></span>
<span data-ttu-id="227d0-124">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="227d0-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="227d0-125">-KeyType</span><span class="sxs-lookup"><span data-stu-id="227d0-125">-KeyType</span></span>
<span data-ttu-id="227d0-126">Hangi tuşun yeniden yeniden kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="227d0-126">Specifies which key to regenerate.</span></span>
<span data-ttu-id="227d0-127">Geçerli değerler: birincil ve Ikincil.</span><span class="sxs-lookup"><span data-stu-id="227d0-127">Valid values are: Primary and Secondary.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="227d0-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="227d0-128">-Profile</span></span>
<span data-ttu-id="227d0-129">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="227d0-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="227d0-130">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="227d0-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="227d0-131">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="227d0-131">-StorageAccountName</span></span>
<span data-ttu-id="227d0-132">Anahtarı yeniden oluşturmak için Azure depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="227d0-132">Specifies the name of the Azure Storage account for which to regenerate a key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="227d0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="227d0-133">CommonParameters</span></span>
<span data-ttu-id="227d0-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="227d0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="227d0-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="227d0-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="227d0-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="227d0-136">INPUTS</span></span>

## <span data-ttu-id="227d0-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="227d0-137">OUTPUTS</span></span>

### <span data-ttu-id="227d0-138">StorageServiceKeys</span><span class="sxs-lookup"><span data-stu-id="227d0-138">StorageServiceKeys</span></span>

## <span data-ttu-id="227d0-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="227d0-139">NOTES</span></span>

## <span data-ttu-id="227d0-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="227d0-140">RELATED LINKS</span></span>

[<span data-ttu-id="227d0-141">Get-AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="227d0-141">Get-AzureStorageKey</span></span>](./Get-AzureStorageKey.md)


