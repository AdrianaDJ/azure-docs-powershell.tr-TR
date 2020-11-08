---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7D7D1FAE-5360-428B-AAE9-9D1109A7B67F
online version: ''
schema: 2.0.0
ms.openlocfilehash: faccd241929beca1f2423fa9c23f35793233205b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105549"
---
# <span data-ttu-id="54be3-101">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="54be3-101">Get-AzureStorageAccount</span></span>

## <span data-ttu-id="54be3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54be3-102">SYNOPSIS</span></span>
<span data-ttu-id="54be3-103">Geçerli Azure aboneliğinin depolama hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="54be3-103">Gets the storage accounts for the current Azure subscription.</span></span>

## <span data-ttu-id="54be3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="54be3-104">SYNTAX</span></span>

```
Get-AzureStorageAccount [[-StorageAccountName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="54be3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="54be3-105">DESCRIPTION</span></span>
<span data-ttu-id="54be3-106">**Get-AzureStorageAccount** cmdlet 'i, geçerli aboneliğin depolama hesapları hakkında bilgi içeren bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="54be3-106">The **Get-AzureStorageAccount** cmdlet returns an object containing information about the storage accounts for the current subscription.</span></span>
<span data-ttu-id="54be3-107">*StorageAccountName* parametresi belirtilmişse, yalnızca belirtilen depolama hesabı hakkında bilgi verilir.</span><span class="sxs-lookup"><span data-stu-id="54be3-107">If the *StorageAccountName* parameter is specified, then only information about the specified storage account is returned.</span></span>

## <span data-ttu-id="54be3-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="54be3-108">EXAMPLES</span></span>

### <span data-ttu-id="54be3-109">Örnek 1: tüm depolama hesaplarını döndürme</span><span class="sxs-lookup"><span data-stu-id="54be3-109">Example 1: Return all storage accounts</span></span>
```
PS C:\> Get-AzureStorageAccount
```

<span data-ttu-id="54be3-110">Bu komut, geçerli abonelikle ilişkilendirilmiş tüm depolama hesaplarını içeren bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="54be3-110">This command returns an object with all the storage accounts associated with the current subscription.</span></span>

### <span data-ttu-id="54be3-111">Örnek 2: belirli bir hesabın hesap bilgilerini döndürme</span><span class="sxs-lookup"><span data-stu-id="54be3-111">Example 2: Return account information for a specified account</span></span>
```
PS C:\> Get-AzureStorageAccount -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="54be3-112">Bu komut, yalnızca ContosoStore01 hesap bilgilerini içeren bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="54be3-112">This command returns an object with only the ContosoStore01 account information.</span></span>

### <span data-ttu-id="54be3-113">Örnek 3: depolama hesapları tablosunu görüntüleme</span><span class="sxs-lookup"><span data-stu-id="54be3-113">Example 3: Display a table of storage accounts</span></span>
```
PS C:\> Get-AzureStorageAccount | Format-Table -AutoSize -Property @{Label="Name";Expression={$_.StorageAccountName}},"Label","Location"
```

<span data-ttu-id="54be3-114">Bu komut geçerli abonelikle ilişkilendirilmiş tüm depolama hesaplarını içeren bir nesne döndürür ve bunları hesap adını, hesap etiketini ve depolama konumunu gösteren bir tablo olarak verir.</span><span class="sxs-lookup"><span data-stu-id="54be3-114">This command returns an object with all the storage accounts associated with the current subscription, and outputs them as a table showing the account name, the account label, and the storage location.</span></span>

## <span data-ttu-id="54be3-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="54be3-115">PARAMETERS</span></span>

### <span data-ttu-id="54be3-116">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="54be3-116">-InformationAction</span></span>
<span data-ttu-id="54be3-117">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="54be3-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="54be3-118">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="54be3-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="54be3-119">'A</span><span class="sxs-lookup"><span data-stu-id="54be3-119">Continue</span></span>
- <span data-ttu-id="54be3-120">Manıza</span><span class="sxs-lookup"><span data-stu-id="54be3-120">Ignore</span></span>
- <span data-ttu-id="54be3-121">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="54be3-121">Inquire</span></span>
- <span data-ttu-id="54be3-122">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="54be3-122">SilentlyContinue</span></span>
- <span data-ttu-id="54be3-123">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="54be3-123">Stop</span></span>
- <span data-ttu-id="54be3-124">Biliriz</span><span class="sxs-lookup"><span data-stu-id="54be3-124">Suspend</span></span>

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

### <span data-ttu-id="54be3-125">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="54be3-125">-InformationVariable</span></span>
<span data-ttu-id="54be3-126">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="54be3-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="54be3-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="54be3-127">-Profile</span></span>
<span data-ttu-id="54be3-128">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="54be3-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="54be3-129">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="54be3-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="54be3-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="54be3-130">-StorageAccountName</span></span>
<span data-ttu-id="54be3-131">Depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="54be3-131">Specifies the name of a storage account.</span></span>
<span data-ttu-id="54be3-132">Belirtilmişse, bu cmdlet yalnızca belirtilen depolama hesabı nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="54be3-132">If specified, this cmdlet returns only the specified storage account object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54be3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54be3-133">CommonParameters</span></span>
<span data-ttu-id="54be3-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="54be3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54be3-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54be3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54be3-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="54be3-136">INPUTS</span></span>

## <span data-ttu-id="54be3-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="54be3-137">OUTPUTS</span></span>

### <span data-ttu-id="54be3-138">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="54be3-138">ManagementOperationContext</span></span>

## <span data-ttu-id="54be3-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="54be3-139">NOTES</span></span>
* <span data-ttu-id="54be3-140">`help node-dev`Geliştirmeyle ilgili yardım almak için Node.js geliştirme ile ilgili yardım alın.</span><span class="sxs-lookup"><span data-stu-id="54be3-140">Type `help node-dev` to get help on Node.js development-related cmdlets.</span></span> <span data-ttu-id="54be3-141">`help php-dev`Php geliştirmeyle ilgili yardım almak için yazın.</span><span class="sxs-lookup"><span data-stu-id="54be3-141">Type `help php-dev` to get help on PHP development-related cmdlets.</span></span>

## <span data-ttu-id="54be3-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="54be3-142">RELATED LINKS</span></span>

[<span data-ttu-id="54be3-143">Yeni-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="54be3-143">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="54be3-144">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="54be3-144">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)


