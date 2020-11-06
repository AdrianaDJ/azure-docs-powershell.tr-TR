---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: f6a9aff40d2cff62e683439b3f28f9e782b2de05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595053"
---
# <span data-ttu-id="4faed-101">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="4faed-101">New-AzureStorageQueue</span></span>

## <span data-ttu-id="4faed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4faed-102">SYNOPSIS</span></span>
<span data-ttu-id="4faed-103">Depolama kuyruğu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4faed-103">Creates a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4faed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4faed-104">SYNTAX</span></span>

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="4faed-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4faed-105">DESCRIPTION</span></span>
<span data-ttu-id="4faed-106">**New-AzureStorageQueue** cmdlet 'i Azure 'da bir depolama sırası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4faed-106">The **New-AzureStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="4faed-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4faed-107">EXAMPLES</span></span>

### <span data-ttu-id="4faed-108">Örnek 1: Azure depolama sırası oluşturma</span><span class="sxs-lookup"><span data-stu-id="4faed-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

<span data-ttu-id="4faed-109">Bu örnek, queueabc adlı bir depolama sırası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4faed-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="4faed-110">Örnek 2: birden çok Azure depolama kuyruğu oluşturma</span><span class="sxs-lookup"><span data-stu-id="4faed-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

<span data-ttu-id="4faed-111">Bu örnek, birden çok depolama sırası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4faed-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="4faed-112">.NET String sınıfının bölme yöntemini kullanır ve sonra da ardışık düzene geçirir.</span><span class="sxs-lookup"><span data-stu-id="4faed-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="4faed-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4faed-113">PARAMETERS</span></span>

### <span data-ttu-id="4faed-114">-Context</span><span class="sxs-lookup"><span data-stu-id="4faed-114">-Context</span></span>
<span data-ttu-id="4faed-115">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4faed-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="4faed-116">Bunu, New-AzureStorageContext cmdlet 'ini kullanarak oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4faed-116">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4faed-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="4faed-117">-Name</span></span>
<span data-ttu-id="4faed-118">Sıra için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="4faed-118">Specifies a name for the queue.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4faed-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4faed-119">CommonParameters</span></span>
<span data-ttu-id="4faed-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4faed-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4faed-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4faed-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4faed-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4faed-122">INPUTS</span></span>

### <span data-ttu-id="4faed-123">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="4faed-123">IStorageContext</span></span>

<span data-ttu-id="4faed-124">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="4faed-124">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="4faed-125">Dizisi</span><span class="sxs-lookup"><span data-stu-id="4faed-125">String</span></span>

<span data-ttu-id="4faed-126">' Name ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="4faed-126">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="4faed-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4faed-127">OUTPUTS</span></span>

### <span data-ttu-id="4faed-128">Microsoft. Windowsazde. Commands. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="4faed-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="4faed-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4faed-129">NOTES</span></span>

## <span data-ttu-id="4faed-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4faed-130">RELATED LINKS</span></span>

[<span data-ttu-id="4faed-131">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="4faed-131">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="4faed-132">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="4faed-132">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


