---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: ebf5596ba63a86e3865c5a6dc05bdea648dc18c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590583"
---
# <span data-ttu-id="76601-101">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="76601-101">Get-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="76601-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76601-102">SYNOPSIS</span></span>
<span data-ttu-id="76601-103">Depolanan erişim ilkesini veya bir Azure depolama sırasının ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="76601-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76601-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="76601-104">SYNTAX</span></span>

```
Get-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="76601-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="76601-105">DESCRIPTION</span></span>
<span data-ttu-id="76601-106">**Get-AzureStorageQueueStoredAccessPolicy** cmdlet 'i Azure depolama sırası için depolanan erişim ilkesini veya ilkelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="76601-106">The **Get-AzureStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="76601-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="76601-107">EXAMPLES</span></span>

### <span data-ttu-id="76601-108">Örnek 1: kuyrukta depolanan bir erişim ilkesi alma</span><span class="sxs-lookup"><span data-stu-id="76601-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="76601-109">Bu komut MyQueue adındaki depolama sırasındaki Policy12 adındaki erişim ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="76601-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="76601-110">Örnek 2: kuyruktaki tüm erişim ilkelerini sıraya alma</span><span class="sxs-lookup"><span data-stu-id="76601-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="76601-111">Bu komut, MyQueue adlı kuyrukta tüm depolanmış erişim ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="76601-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="76601-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="76601-112">PARAMETERS</span></span>

### <span data-ttu-id="76601-113">-Context</span><span class="sxs-lookup"><span data-stu-id="76601-113">-Context</span></span>
<span data-ttu-id="76601-114">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="76601-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="76601-115">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="76601-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="76601-116">-İlke</span><span class="sxs-lookup"><span data-stu-id="76601-116">-Policy</span></span>
<span data-ttu-id="76601-117">Bu paylaşılan erişim Imzası (SAS) belirtecinin izinlerini içeren depolanan bir erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="76601-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="76601-118">-Sıra</span><span class="sxs-lookup"><span data-stu-id="76601-118">-Queue</span></span>
<span data-ttu-id="76601-119">Azure depolama sırası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="76601-119">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="76601-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76601-120">CommonParameters</span></span>
<span data-ttu-id="76601-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="76601-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76601-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76601-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76601-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="76601-123">INPUTS</span></span>

### <span data-ttu-id="76601-124">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="76601-124">IStorageContext</span></span>

<span data-ttu-id="76601-125">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="76601-125">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="76601-126">Dizisi</span><span class="sxs-lookup"><span data-stu-id="76601-126">String</span></span>

<span data-ttu-id="76601-127">' Queue ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="76601-127">Parameter 'Queue' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="76601-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="76601-128">OUTPUTS</span></span>

### <span data-ttu-id="76601-129">Microsoft. Windowsazde. Storage. Queue. SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="76601-129">Microsoft.WindowsAzure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="76601-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="76601-130">NOTES</span></span>

## <span data-ttu-id="76601-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="76601-131">RELATED LINKS</span></span>

[<span data-ttu-id="76601-132">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="76601-132">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="76601-133">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="76601-133">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="76601-134">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="76601-134">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="76601-135">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="76601-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


