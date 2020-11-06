---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueue.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 3fe38645f4903e2020199b10b277da856046ac59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592696"
---
# <span data-ttu-id="cd25e-101">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="cd25e-101">Get-AzureStorageQueue</span></span>

## <span data-ttu-id="cd25e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd25e-102">SYNOPSIS</span></span>
<span data-ttu-id="cd25e-103">Depolama sıralarını listeler.</span><span class="sxs-lookup"><span data-stu-id="cd25e-103">Lists storage queues.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd25e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cd25e-104">SYNTAX</span></span>

### <span data-ttu-id="cd25e-105">SıraAdı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cd25e-105">QueueName (Default)</span></span>
```
Get-AzureStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="cd25e-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="cd25e-106">QueuePrefix</span></span>
```
Get-AzureStorageQueue -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="cd25e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="cd25e-107">DESCRIPTION</span></span>
<span data-ttu-id="cd25e-108">**Get-AzureStorageQueue** cmdlet 'ı bir Azure depolama hesabıyla ilişkilendirilmiş depolama sıralarını listeler.</span><span class="sxs-lookup"><span data-stu-id="cd25e-108">The **Get-AzureStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="cd25e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cd25e-109">EXAMPLES</span></span>

### <span data-ttu-id="cd25e-110">Örnek 1: tüm Azure depolama sıralarını listeler</span><span class="sxs-lookup"><span data-stu-id="cd25e-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue
```

<span data-ttu-id="cd25e-111">Bu komut, geçerli depolama hesabının tüm depolama sıralarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="cd25e-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="cd25e-112">Örnek 2: joker karakter kullanarak Azure depolama sıralarını listeleme</span><span class="sxs-lookup"><span data-stu-id="cd25e-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageQueue -Name queue*
```

<span data-ttu-id="cd25e-113">Bu komut, adı sırayla başlayan depolama sıralarının listesini almak için joker karakter kullanır.</span><span class="sxs-lookup"><span data-stu-id="cd25e-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="cd25e-114">Örnek 3: sıra adı önekini kullanarak Azure depolama sıralarını listeleme</span><span class="sxs-lookup"><span data-stu-id="cd25e-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzureStorageQueue -Prefix "queue"
```

<span data-ttu-id="cd25e-115">Bu örnekte, adı sırayla başlayan depolama sıralarının listesini almak için *önek* parametresi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="cd25e-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="cd25e-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cd25e-116">PARAMETERS</span></span>

### <span data-ttu-id="cd25e-117">-Context</span><span class="sxs-lookup"><span data-stu-id="cd25e-117">-Context</span></span>
<span data-ttu-id="cd25e-118">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd25e-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="cd25e-119">Bunu **New-AzureStorageContext** cmdlet 'i kullanarak oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cd25e-119">You can create it by using the **New-AzureStorageContext** cmdlet.</span></span>

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

### <span data-ttu-id="cd25e-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="cd25e-120">-Name</span></span>
<span data-ttu-id="cd25e-121">Bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd25e-121">Specifies a name.</span></span>
<span data-ttu-id="cd25e-122">Ad belirtilmezse cmdlet, tüm sıraların listesini alır.</span><span class="sxs-lookup"><span data-stu-id="cd25e-122">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="cd25e-123">Tam veya kısmi ad belirtilirse cmdlet, Ad düzeniyle eşleşen tüm sıraları alır.</span><span class="sxs-lookup"><span data-stu-id="cd25e-123">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

```yaml
Type: String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="cd25e-124">-Önek</span><span class="sxs-lookup"><span data-stu-id="cd25e-124">-Prefix</span></span>
<span data-ttu-id="cd25e-125">Almak istediğiniz sıraların adında kullanılan bir önek belirtir.</span><span class="sxs-lookup"><span data-stu-id="cd25e-125">Specifies a prefix used in the name of the queues you want to get.</span></span>

```yaml
Type: String
Parameter Sets: QueuePrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd25e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd25e-126">CommonParameters</span></span>
<span data-ttu-id="cd25e-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cd25e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd25e-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd25e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd25e-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cd25e-129">INPUTS</span></span>

### <span data-ttu-id="cd25e-130">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="cd25e-130">IStorageContext</span></span>

<span data-ttu-id="cd25e-131">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="cd25e-131">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="cd25e-132">Dizisi</span><span class="sxs-lookup"><span data-stu-id="cd25e-132">String</span></span>

<span data-ttu-id="cd25e-133">' Name ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="cd25e-133">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="cd25e-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cd25e-134">OUTPUTS</span></span>

### <span data-ttu-id="cd25e-135">Microsoft. Windowsazde. Commands. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="cd25e-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="cd25e-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cd25e-136">NOTES</span></span>

## <span data-ttu-id="cd25e-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cd25e-137">RELATED LINKS</span></span>

[<span data-ttu-id="cd25e-138">Yeni-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="cd25e-138">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)

[<span data-ttu-id="cd25e-139">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="cd25e-139">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


