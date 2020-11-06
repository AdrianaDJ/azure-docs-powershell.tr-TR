---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 76876cb76e65c913401d62fc7f08b3cb8b5626c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572014"
---
# <span data-ttu-id="12302-101">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="12302-101">New-AzureStorageQueue</span></span>

## <span data-ttu-id="12302-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12302-102">SYNOPSIS</span></span>
<span data-ttu-id="12302-103">Depolama kuyruğu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="12302-103">Creates a storage queue.</span></span>

## <span data-ttu-id="12302-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="12302-104">SYNTAX</span></span>

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="12302-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="12302-105">DESCRIPTION</span></span>
<span data-ttu-id="12302-106">**New-AzureStorageQueue** cmdlet 'i Azure 'da bir depolama sırası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="12302-106">The **New-AzureStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="12302-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="12302-107">EXAMPLES</span></span>

### <span data-ttu-id="12302-108">Örnek 1: Azure depolama sırası oluşturma</span><span class="sxs-lookup"><span data-stu-id="12302-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

<span data-ttu-id="12302-109">Bu örnek, queueabc adlı bir depolama sırası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="12302-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="12302-110">Örnek 2: birden çok Azure depolama kuyruğu oluşturma</span><span class="sxs-lookup"><span data-stu-id="12302-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

<span data-ttu-id="12302-111">Bu örnek, birden çok depolama sırası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="12302-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="12302-112">.NET String sınıfının bölme yöntemini kullanır ve sonra da ardışık düzene geçirir.</span><span class="sxs-lookup"><span data-stu-id="12302-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="12302-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="12302-113">PARAMETERS</span></span>

### <span data-ttu-id="12302-114">-Context</span><span class="sxs-lookup"><span data-stu-id="12302-114">-Context</span></span>
<span data-ttu-id="12302-115">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="12302-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="12302-116">Bunu, New-AzureStorageContext cmdlet 'ini kullanarak oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="12302-116">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="12302-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="12302-117">-Name</span></span>
<span data-ttu-id="12302-118">Sıra için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="12302-118">Specifies a name for the queue.</span></span>

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

### <span data-ttu-id="12302-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12302-119">CommonParameters</span></span>
<span data-ttu-id="12302-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="12302-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12302-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12302-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12302-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="12302-122">INPUTS</span></span>

## <span data-ttu-id="12302-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="12302-123">OUTPUTS</span></span>

## <span data-ttu-id="12302-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="12302-124">NOTES</span></span>

## <span data-ttu-id="12302-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="12302-125">RELATED LINKS</span></span>

[<span data-ttu-id="12302-126">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="12302-126">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="12302-127">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="12302-127">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


