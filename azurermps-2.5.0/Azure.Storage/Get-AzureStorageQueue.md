---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragequeue
schema: 2.0.0
ms.openlocfilehash: 59a035a7af56a333a1ef91b5ce4aa2d1afbe5086
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940223"
---
# <span data-ttu-id="b0a94-101">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="b0a94-101">Get-AzureStorageQueue</span></span>

## <span data-ttu-id="b0a94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0a94-102">SYNOPSIS</span></span>
<span data-ttu-id="b0a94-103">Depolama sıralarını listeler.</span><span class="sxs-lookup"><span data-stu-id="b0a94-103">Lists storage queues.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0a94-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b0a94-104">SYNTAX</span></span>

### <span data-ttu-id="b0a94-105">SıraAdı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b0a94-105">QueueName (Default)</span></span>
```
Get-AzureStorageQueue [[-Name] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0a94-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="b0a94-106">QueuePrefix</span></span>
```
Get-AzureStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b0a94-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b0a94-107">DESCRIPTION</span></span>
<span data-ttu-id="b0a94-108">**Get-AzureStorageQueue** cmdlet 'ı bir Azure depolama hesabıyla ilişkilendirilmiş depolama sıralarını listeler.</span><span class="sxs-lookup"><span data-stu-id="b0a94-108">The **Get-AzureStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="b0a94-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b0a94-109">EXAMPLES</span></span>

### <span data-ttu-id="b0a94-110">Örnek 1: tüm Azure depolama sıralarını listeler</span><span class="sxs-lookup"><span data-stu-id="b0a94-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue
```

<span data-ttu-id="b0a94-111">Bu komut, geçerli depolama hesabının tüm depolama sıralarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="b0a94-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="b0a94-112">Örnek 2: joker karakter kullanarak Azure depolama sıralarını listeleme</span><span class="sxs-lookup"><span data-stu-id="b0a94-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageQueue -Name queue*
```

<span data-ttu-id="b0a94-113">Bu komut, adı sırayla başlayan depolama sıralarının listesini almak için joker karakter kullanır.</span><span class="sxs-lookup"><span data-stu-id="b0a94-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="b0a94-114">Örnek 3: sıra adı önekini kullanarak Azure depolama sıralarını listeleme</span><span class="sxs-lookup"><span data-stu-id="b0a94-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzureStorageQueue -Prefix "queue"
```

<span data-ttu-id="b0a94-115">Bu örnekte, adı sırayla başlayan depolama sıralarının listesini almak için *önek* parametresi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b0a94-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="b0a94-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b0a94-116">PARAMETERS</span></span>

### <span data-ttu-id="b0a94-117">-Context</span><span class="sxs-lookup"><span data-stu-id="b0a94-117">-Context</span></span>
<span data-ttu-id="b0a94-118">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b0a94-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="b0a94-119">Bunu **New-AzureStorageContext** cmdlet 'i kullanarak oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b0a94-119">You can create it by using the **New-AzureStorageContext** cmdlet.</span></span>

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

### <span data-ttu-id="b0a94-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0a94-120">-DefaultProfile</span></span>
<span data-ttu-id="b0a94-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b0a94-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0a94-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="b0a94-122">-Name</span></span>
<span data-ttu-id="b0a94-123">Bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="b0a94-123">Specifies a name.</span></span>
<span data-ttu-id="b0a94-124">Ad belirtilmezse cmdlet, tüm sıraların listesini alır.</span><span class="sxs-lookup"><span data-stu-id="b0a94-124">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="b0a94-125">Tam veya kısmi ad belirtilirse cmdlet, Ad düzeniyle eşleşen tüm sıraları alır.</span><span class="sxs-lookup"><span data-stu-id="b0a94-125">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

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

### <span data-ttu-id="b0a94-126">-Önek</span><span class="sxs-lookup"><span data-stu-id="b0a94-126">-Prefix</span></span>
<span data-ttu-id="b0a94-127">Almak istediğiniz sıraların adında kullanılan bir önek belirtir.</span><span class="sxs-lookup"><span data-stu-id="b0a94-127">Specifies a prefix used in the name of the queues you want to get.</span></span>

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

### <span data-ttu-id="b0a94-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0a94-128">CommonParameters</span></span>
<span data-ttu-id="b0a94-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b0a94-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0a94-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0a94-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0a94-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b0a94-131">INPUTS</span></span>

### <span data-ttu-id="b0a94-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b0a94-132">System.String</span></span>

### <span data-ttu-id="b0a94-133">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="b0a94-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b0a94-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b0a94-134">OUTPUTS</span></span>

### <span data-ttu-id="b0a94-135">Microsoft. Windowsazde. Commands. Common. Storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="b0a94-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="b0a94-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b0a94-136">NOTES</span></span>

## <span data-ttu-id="b0a94-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b0a94-137">RELATED LINKS</span></span>

[<span data-ttu-id="b0a94-138">Yeni-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="b0a94-138">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)

[<span data-ttu-id="b0a94-139">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="b0a94-139">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


