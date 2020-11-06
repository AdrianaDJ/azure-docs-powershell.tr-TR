---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: ''
schema: 2.0.0
ms.openlocfilehash: 552b1e638034cf0cec5825b742af4984b688cec3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572369"
---
# <span data-ttu-id="86916-101">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="86916-101">Get-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="86916-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86916-102">SYNOPSIS</span></span>
<span data-ttu-id="86916-103">Depolanan erişim ilkesini veya bir Azure depolama sırasının ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="86916-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="86916-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="86916-104">SYNTAX</span></span>

```
Get-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="86916-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="86916-105">DESCRIPTION</span></span>
<span data-ttu-id="86916-106">**Get-AzureStorageQueueStoredAccessPolicy** cmdlet 'i Azure depolama sırası için depolanan erişim ilkesini veya ilkelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="86916-106">The **Get-AzureStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="86916-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="86916-107">EXAMPLES</span></span>

### <span data-ttu-id="86916-108">Örnek 1: kuyrukta depolanan bir erişim ilkesi alma</span><span class="sxs-lookup"><span data-stu-id="86916-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="86916-109">Bu komut MyQueue adındaki depolama sırasındaki Policy12 adındaki erişim ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="86916-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="86916-110">Örnek 2: kuyruktaki tüm erişim ilkelerini sıraya alma</span><span class="sxs-lookup"><span data-stu-id="86916-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="86916-111">Bu komut, MyQueue adlı kuyrukta tüm depolanmış erişim ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="86916-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="86916-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="86916-112">PARAMETERS</span></span>

### <span data-ttu-id="86916-113">-Context</span><span class="sxs-lookup"><span data-stu-id="86916-113">-Context</span></span>
<span data-ttu-id="86916-114">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="86916-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="86916-115">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="86916-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="86916-116">-İlke</span><span class="sxs-lookup"><span data-stu-id="86916-116">-Policy</span></span>
<span data-ttu-id="86916-117">Bu paylaşılan erişim Imzası (SAS) belirtecinin izinlerini içeren depolanan bir erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="86916-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="86916-118">-Sıra</span><span class="sxs-lookup"><span data-stu-id="86916-118">-Queue</span></span>
<span data-ttu-id="86916-119">Azure depolama sırası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="86916-119">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="86916-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86916-120">CommonParameters</span></span>
<span data-ttu-id="86916-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="86916-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86916-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86916-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86916-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="86916-123">INPUTS</span></span>

## <span data-ttu-id="86916-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="86916-124">OUTPUTS</span></span>

## <span data-ttu-id="86916-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="86916-125">NOTES</span></span>

## <span data-ttu-id="86916-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="86916-126">RELATED LINKS</span></span>

[<span data-ttu-id="86916-127">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="86916-127">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="86916-128">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="86916-128">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="86916-129">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="86916-129">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="86916-130">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="86916-130">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


