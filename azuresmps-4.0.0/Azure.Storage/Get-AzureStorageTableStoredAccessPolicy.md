---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8c22b3eb95ab940670043f9ae467663c951027d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572341"
---
# <span data-ttu-id="a7aed-101">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a7aed-101">Get-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="a7aed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7aed-102">SYNOPSIS</span></span>
<span data-ttu-id="a7aed-103">Azure depolama tablosu için depolanan erişim ilkesini veya ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="a7aed-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="a7aed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a7aed-104">SYNTAX</span></span>

```
Get-AzureStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7aed-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a7aed-105">DESCRIPTION</span></span>
<span data-ttu-id="a7aed-106">**Get-AzureStorageTableStoredAccessPolicy** cmdlet 'i, bir Azure depolama tablosu için depolanan erişim ilkesini veya ilkelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="a7aed-106">The **Get-AzureStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="a7aed-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a7aed-107">EXAMPLES</span></span>

### <span data-ttu-id="a7aed-108">Örnek 1: depolama tablosunda depolanan bir erişim ilkesi alma</span><span class="sxs-lookup"><span data-stu-id="a7aed-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="a7aed-109">Bu komut, Table02 adındaki depolama tablosundaki Policy50 adındaki erişim ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="a7aed-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="a7aed-110">Örnek 2: depolama tablosunda tüm depolanan erişim ilkelerini alma</span><span class="sxs-lookup"><span data-stu-id="a7aed-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="a7aed-111">Bu komut, Table02 adlı tablodaki tüm erişim ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="a7aed-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="a7aed-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a7aed-112">PARAMETERS</span></span>

### <span data-ttu-id="a7aed-113">-Context</span><span class="sxs-lookup"><span data-stu-id="a7aed-113">-Context</span></span>
<span data-ttu-id="a7aed-114">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a7aed-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="a7aed-115">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a7aed-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7aed-116">-İlke</span><span class="sxs-lookup"><span data-stu-id="a7aed-116">-Policy</span></span>
<span data-ttu-id="a7aed-117">Bu paylaşılan erişim Imzası (SAS) belirtecinin izinlerini içeren depolanan bir erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a7aed-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7aed-118">-Tablo</span><span class="sxs-lookup"><span data-stu-id="a7aed-118">-Table</span></span>
<span data-ttu-id="a7aed-119">Azure depolama tablosu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a7aed-119">Specifies the Azure storage table name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7aed-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7aed-120">CommonParameters</span></span>
<span data-ttu-id="a7aed-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a7aed-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7aed-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7aed-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7aed-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a7aed-123">INPUTS</span></span>

## <span data-ttu-id="a7aed-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a7aed-124">OUTPUTS</span></span>

## <span data-ttu-id="a7aed-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a7aed-125">NOTES</span></span>

## <span data-ttu-id="a7aed-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a7aed-126">RELATED LINKS</span></span>

[<span data-ttu-id="a7aed-127">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a7aed-127">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="a7aed-128">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a7aed-128">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="a7aed-129">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a7aed-129">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="a7aed-130">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="a7aed-130">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


