---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTableStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 85501affef70ce0cf31e62f9083d5ed383425497
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762081"
---
# <span data-ttu-id="7c4a3-101">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7c4a3-101">Get-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="7c4a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c4a3-102">SYNOPSIS</span></span>
<span data-ttu-id="7c4a3-103">Azure depolama tablosu için depolanan erişim ilkesini veya ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="7c4a3-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c4a3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7c4a3-104">SYNTAX</span></span>

```
Get-AzureStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="7c4a3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7c4a3-105">DESCRIPTION</span></span>
<span data-ttu-id="7c4a3-106">**Get-AzureStorageTableStoredAccessPolicy** cmdlet 'i, bir Azure depolama tablosu için depolanan erişim ilkesini veya ilkelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="7c4a3-106">The **Get-AzureStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="7c4a3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7c4a3-107">EXAMPLES</span></span>

### <span data-ttu-id="7c4a3-108">Örnek 1: depolama tablosunda depolanan bir erişim ilkesi alma</span><span class="sxs-lookup"><span data-stu-id="7c4a3-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="7c4a3-109">Bu komut, Table02 adındaki depolama tablosundaki Policy50 adındaki erişim ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="7c4a3-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="7c4a3-110">Örnek 2: depolama tablosunda tüm depolanan erişim ilkelerini alma</span><span class="sxs-lookup"><span data-stu-id="7c4a3-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="7c4a3-111">Bu komut, Table02 adlı tablodaki tüm erişim ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="7c4a3-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="7c4a3-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7c4a3-112">PARAMETERS</span></span>

### <span data-ttu-id="7c4a3-113">-Context</span><span class="sxs-lookup"><span data-stu-id="7c4a3-113">-Context</span></span>
<span data-ttu-id="7c4a3-114">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7c4a3-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="7c4a3-115">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7c4a3-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="7c4a3-116">-İlke</span><span class="sxs-lookup"><span data-stu-id="7c4a3-116">-Policy</span></span>
<span data-ttu-id="7c4a3-117">Bu paylaşılan erişim Imzası (SAS) belirtecinin izinlerini içeren depolanan bir erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7c4a3-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="7c4a3-118">-Tablo</span><span class="sxs-lookup"><span data-stu-id="7c4a3-118">-Table</span></span>
<span data-ttu-id="7c4a3-119">Azure depolama tablosu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7c4a3-119">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="7c4a3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c4a3-120">CommonParameters</span></span>
<span data-ttu-id="7c4a3-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7c4a3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c4a3-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c4a3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c4a3-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7c4a3-123">INPUTS</span></span>

### <span data-ttu-id="7c4a3-124">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="7c4a3-124">IStorageContext</span></span>

<span data-ttu-id="7c4a3-125">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="7c4a3-125">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="7c4a3-126">Dizisi</span><span class="sxs-lookup"><span data-stu-id="7c4a3-126">String</span></span>

<span data-ttu-id="7c4a3-127">Parametre ' tablosu ', ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="7c4a3-127">Parameter 'Table' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="7c4a3-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7c4a3-128">OUTPUTS</span></span>

### <span data-ttu-id="7c4a3-129">Microsoft. Windowsazde. Storage. Table. SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="7c4a3-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="7c4a3-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7c4a3-130">NOTES</span></span>

## <span data-ttu-id="7c4a3-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7c4a3-131">RELATED LINKS</span></span>

[<span data-ttu-id="7c4a3-132">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7c4a3-132">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="7c4a3-133">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7c4a3-133">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="7c4a3-134">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7c4a3-134">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="7c4a3-135">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="7c4a3-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


