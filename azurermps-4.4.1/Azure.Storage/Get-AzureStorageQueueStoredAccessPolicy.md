---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueueStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 78815aaa29c46e455f24ce0daac167b2806b6c20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763417"
---
# <span data-ttu-id="5f025-101">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5f025-101">Get-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="5f025-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f025-102">SYNOPSIS</span></span>
<span data-ttu-id="5f025-103">Depolanan erişim ilkesini veya bir Azure depolama sırasının ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="5f025-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f025-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5f025-104">SYNTAX</span></span>

```
Get-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f025-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5f025-105">DESCRIPTION</span></span>
<span data-ttu-id="5f025-106">**Get-AzureStorageQueueStoredAccessPolicy** cmdlet 'i Azure depolama sırası için depolanan erişim ilkesini veya ilkelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="5f025-106">The **Get-AzureStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="5f025-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5f025-107">EXAMPLES</span></span>

### <span data-ttu-id="5f025-108">Örnek 1: kuyrukta depolanan bir erişim ilkesi alma</span><span class="sxs-lookup"><span data-stu-id="5f025-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="5f025-109">Bu komut MyQueue adındaki depolama sırasındaki Policy12 adındaki erişim ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="5f025-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="5f025-110">Örnek 2: kuyruktaki tüm erişim ilkelerini sıraya alma</span><span class="sxs-lookup"><span data-stu-id="5f025-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="5f025-111">Bu komut, MyQueue adlı kuyrukta tüm depolanmış erişim ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="5f025-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="5f025-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5f025-112">PARAMETERS</span></span>

### <span data-ttu-id="5f025-113">-Context</span><span class="sxs-lookup"><span data-stu-id="5f025-113">-Context</span></span>
<span data-ttu-id="5f025-114">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5f025-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="5f025-115">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5f025-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="5f025-116">-İlke</span><span class="sxs-lookup"><span data-stu-id="5f025-116">-Policy</span></span>
<span data-ttu-id="5f025-117">Bu paylaşılan erişim Imzası (SAS) belirtecinin izinlerini içeren depolanan bir erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5f025-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="5f025-118">-Sıra</span><span class="sxs-lookup"><span data-stu-id="5f025-118">-Queue</span></span>
<span data-ttu-id="5f025-119">Azure depolama sırası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5f025-119">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="5f025-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f025-120">CommonParameters</span></span>
<span data-ttu-id="5f025-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5f025-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f025-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f025-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f025-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5f025-123">INPUTS</span></span>

### <span data-ttu-id="5f025-124">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="5f025-124">IStorageContext</span></span>

<span data-ttu-id="5f025-125">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="5f025-125">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="5f025-126">Dizisi</span><span class="sxs-lookup"><span data-stu-id="5f025-126">String</span></span>

<span data-ttu-id="5f025-127">' Queue ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="5f025-127">Parameter 'Queue' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="5f025-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5f025-128">OUTPUTS</span></span>

### <span data-ttu-id="5f025-129">Microsoft. Windowsazde. Storage. Queue. SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="5f025-129">Microsoft.WindowsAzure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="5f025-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5f025-130">NOTES</span></span>

## <span data-ttu-id="5f025-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5f025-131">RELATED LINKS</span></span>

[<span data-ttu-id="5f025-132">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5f025-132">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="5f025-133">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5f025-133">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="5f025-134">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5f025-134">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="5f025-135">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="5f025-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


