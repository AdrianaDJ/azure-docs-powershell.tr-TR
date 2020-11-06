---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
ms.openlocfilehash: 62fc501c267e388498cb1563206d2efac083c058
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588665"
---
# <span data-ttu-id="df169-101">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="df169-101">New-AzureStorageQueue</span></span>

## <span data-ttu-id="df169-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df169-102">SYNOPSIS</span></span>
<span data-ttu-id="df169-103">Depolama kuyruğu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="df169-103">Creates a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df169-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="df169-104">SYNTAX</span></span>

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df169-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="df169-105">DESCRIPTION</span></span>
<span data-ttu-id="df169-106">**New-AzureStorageQueue** cmdlet 'i Azure 'da bir depolama sırası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="df169-106">The **New-AzureStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="df169-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="df169-107">EXAMPLES</span></span>

### <span data-ttu-id="df169-108">Örnek 1: Azure depolama sırası oluşturma</span><span class="sxs-lookup"><span data-stu-id="df169-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

<span data-ttu-id="df169-109">Bu örnek, queueabc adlı bir depolama sırası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="df169-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="df169-110">Örnek 2: birden çok Azure depolama kuyruğu oluşturma</span><span class="sxs-lookup"><span data-stu-id="df169-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

<span data-ttu-id="df169-111">Bu örnek, birden çok depolama sırası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="df169-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="df169-112">.NET String sınıfının bölme yöntemini kullanır ve sonra da ardışık düzene geçirir.</span><span class="sxs-lookup"><span data-stu-id="df169-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="df169-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="df169-113">PARAMETERS</span></span>

### <span data-ttu-id="df169-114">-Context</span><span class="sxs-lookup"><span data-stu-id="df169-114">-Context</span></span>
<span data-ttu-id="df169-115">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="df169-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="df169-116">Bunu, New-AzureStorageContext cmdlet 'ini kullanarak oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="df169-116">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df169-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df169-117">-DefaultProfile</span></span>
<span data-ttu-id="df169-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="df169-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df169-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="df169-119">-Name</span></span>
<span data-ttu-id="df169-120">Sıra için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="df169-120">Specifies a name for the queue.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df169-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df169-121">CommonParameters</span></span>
<span data-ttu-id="df169-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="df169-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df169-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df169-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df169-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="df169-124">INPUTS</span></span>

### <span data-ttu-id="df169-125">System. String</span><span class="sxs-lookup"><span data-stu-id="df169-125">System.String</span></span>

### <span data-ttu-id="df169-126">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="df169-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="df169-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="df169-127">OUTPUTS</span></span>

### <span data-ttu-id="df169-128">Microsoft. Windowsazde. Commands. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="df169-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="df169-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="df169-129">NOTES</span></span>

## <span data-ttu-id="df169-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="df169-130">RELATED LINKS</span></span>

[<span data-ttu-id="df169-131">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="df169-131">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="df169-132">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="df169-132">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


