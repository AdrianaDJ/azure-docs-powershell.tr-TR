---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
ms.openlocfilehash: df6f616aacb066ec17aa089b8d91226a5bd171b8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758607"
---
# <span data-ttu-id="ee9c4-101">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="ee9c4-101">New-AzStorageQueue</span></span>

## <span data-ttu-id="ee9c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee9c4-102">SYNOPSIS</span></span>
<span data-ttu-id="ee9c4-103">Depolama kuyruğu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ee9c4-103">Creates a storage queue.</span></span>

## <span data-ttu-id="ee9c4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ee9c4-104">SYNTAX</span></span>

```
New-AzStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ee9c4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ee9c4-105">DESCRIPTION</span></span>
<span data-ttu-id="ee9c4-106">**New-AzStorageQueue** cmdlet 'i Azure 'da bir depolama sırası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ee9c4-106">The **New-AzStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="ee9c4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ee9c4-107">EXAMPLES</span></span>

### <span data-ttu-id="ee9c4-108">Örnek 1: Azure depolama sırası oluşturma</span><span class="sxs-lookup"><span data-stu-id="ee9c4-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzStorageQueue -Name "queueabc"
```

<span data-ttu-id="ee9c4-109">Bu örnek, queueabc adlı bir depolama sırası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ee9c4-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="ee9c4-110">Örnek 2: birden çok Azure depolama kuyruğu oluşturma</span><span class="sxs-lookup"><span data-stu-id="ee9c4-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzStorageQueue
```

<span data-ttu-id="ee9c4-111">Bu örnek, birden çok depolama sırası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ee9c4-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="ee9c4-112">.NET String sınıfının bölme yöntemini kullanır ve sonra da ardışık düzene geçirir.</span><span class="sxs-lookup"><span data-stu-id="ee9c4-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="ee9c4-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ee9c4-113">PARAMETERS</span></span>

### <span data-ttu-id="ee9c4-114">-Context</span><span class="sxs-lookup"><span data-stu-id="ee9c4-114">-Context</span></span>
<span data-ttu-id="ee9c4-115">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee9c4-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="ee9c4-116">Bunu, New-AzStorageContext cmdlet 'ini kullanarak oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ee9c4-116">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ee9c4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee9c4-117">-DefaultProfile</span></span>
<span data-ttu-id="ee9c4-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ee9c4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee9c4-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="ee9c4-119">-Name</span></span>
<span data-ttu-id="ee9c4-120">Sıra için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee9c4-120">Specifies a name for the queue.</span></span>

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

### <span data-ttu-id="ee9c4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee9c4-121">CommonParameters</span></span>
<span data-ttu-id="ee9c4-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ee9c4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee9c4-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee9c4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee9c4-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ee9c4-124">INPUTS</span></span>

### <span data-ttu-id="ee9c4-125">System. String</span><span class="sxs-lookup"><span data-stu-id="ee9c4-125">System.String</span></span>

### <span data-ttu-id="ee9c4-126">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="ee9c4-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ee9c4-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ee9c4-127">OUTPUTS</span></span>

### <span data-ttu-id="ee9c4-128">Microsoft. Windowsazde. Commands. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="ee9c4-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="ee9c4-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ee9c4-129">NOTES</span></span>

## <span data-ttu-id="ee9c4-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ee9c4-130">RELATED LINKS</span></span>

[<span data-ttu-id="ee9c4-131">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="ee9c4-131">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="ee9c4-132">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="ee9c4-132">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)


