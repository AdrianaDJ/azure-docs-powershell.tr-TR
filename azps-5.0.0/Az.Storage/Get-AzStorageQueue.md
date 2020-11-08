---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
ms.openlocfilehash: df4d31c1a90808e4d289cab60c5edf9785de1182
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276345"
---
# <span data-ttu-id="8916a-101">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="8916a-101">Get-AzStorageQueue</span></span>

## <span data-ttu-id="8916a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8916a-102">SYNOPSIS</span></span>
<span data-ttu-id="8916a-103">Depolama sıralarını listeler.</span><span class="sxs-lookup"><span data-stu-id="8916a-103">Lists storage queues.</span></span>

## <span data-ttu-id="8916a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8916a-104">SYNTAX</span></span>

### <span data-ttu-id="8916a-105">SıraAdı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8916a-105">QueueName (Default)</span></span>
```
Get-AzStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8916a-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="8916a-106">QueuePrefix</span></span>
```
Get-AzStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8916a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8916a-107">DESCRIPTION</span></span>
<span data-ttu-id="8916a-108">**Get-AzStorageQueue** cmdlet 'ı, Azure depolama hesabıyla ilişkilendirilmiş depolama sıralarını listeler.</span><span class="sxs-lookup"><span data-stu-id="8916a-108">The **Get-AzStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="8916a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8916a-109">EXAMPLES</span></span>

### <span data-ttu-id="8916a-110">Örnek 1: tüm Azure depolama sıralarını listeler</span><span class="sxs-lookup"><span data-stu-id="8916a-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzStorageQueue
```

<span data-ttu-id="8916a-111">Bu komut, geçerli depolama hesabının tüm depolama sıralarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="8916a-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="8916a-112">Örnek 2: joker karakter kullanarak Azure depolama sıralarını listeleme</span><span class="sxs-lookup"><span data-stu-id="8916a-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzStorageQueue -Name queue*
```

<span data-ttu-id="8916a-113">Bu komut, adı sırayla başlayan depolama sıralarının listesini almak için joker karakter kullanır.</span><span class="sxs-lookup"><span data-stu-id="8916a-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="8916a-114">Örnek 3: sıra adı önekini kullanarak Azure depolama sıralarını listeleme</span><span class="sxs-lookup"><span data-stu-id="8916a-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzStorageQueue -Prefix "queue"
```

<span data-ttu-id="8916a-115">Bu örnekte, adı sırayla başlayan depolama sıralarının listesini almak için *önek* parametresi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8916a-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="8916a-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8916a-116">PARAMETERS</span></span>

### <span data-ttu-id="8916a-117">-Context</span><span class="sxs-lookup"><span data-stu-id="8916a-117">-Context</span></span>
<span data-ttu-id="8916a-118">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8916a-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="8916a-119">Bunu, **New-AzStorageContext** cmdlet 'ini kullanarak oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8916a-119">You can create it by using the **New-AzStorageContext** cmdlet.</span></span>

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

### <span data-ttu-id="8916a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8916a-120">-DefaultProfile</span></span>
<span data-ttu-id="8916a-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8916a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8916a-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="8916a-122">-Name</span></span>
<span data-ttu-id="8916a-123">Bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="8916a-123">Specifies a name.</span></span>
<span data-ttu-id="8916a-124">Ad belirtilmezse cmdlet, tüm sıraların listesini alır.</span><span class="sxs-lookup"><span data-stu-id="8916a-124">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="8916a-125">Tam veya kısmi ad belirtilirse cmdlet, Ad düzeniyle eşleşen tüm sıraları alır.</span><span class="sxs-lookup"><span data-stu-id="8916a-125">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

```yaml
Type: System.String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8916a-126">-Önek</span><span class="sxs-lookup"><span data-stu-id="8916a-126">-Prefix</span></span>
<span data-ttu-id="8916a-127">Almak istediğiniz sıraların adında kullanılan bir önek belirtir.</span><span class="sxs-lookup"><span data-stu-id="8916a-127">Specifies a prefix used in the name of the queues you want to get.</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8916a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8916a-128">CommonParameters</span></span>
<span data-ttu-id="8916a-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8916a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8916a-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8916a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8916a-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8916a-131">INPUTS</span></span>

### <span data-ttu-id="8916a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8916a-132">System.String</span></span>

### <span data-ttu-id="8916a-133">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="8916a-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8916a-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8916a-134">OUTPUTS</span></span>

### <span data-ttu-id="8916a-135">Microsoft. Windowsazde. Commands. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="8916a-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="8916a-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8916a-136">NOTES</span></span>

## <span data-ttu-id="8916a-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8916a-137">RELATED LINKS</span></span>

[<span data-ttu-id="8916a-138">Yeni-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="8916a-138">New-AzStorageQueue</span></span>](./New-AzStorageQueue.md)

[<span data-ttu-id="8916a-139">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="8916a-139">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)


