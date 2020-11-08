---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: b1e7f305b571c5b40c12dacadf520f9637e076f3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276341"
---
# <span data-ttu-id="d0703-101">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d0703-101">Get-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="d0703-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0703-102">SYNOPSIS</span></span>
<span data-ttu-id="d0703-103">Depolanan erişim ilkesini veya bir Azure depolama sırasının ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="d0703-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="d0703-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d0703-104">SYNTAX</span></span>

```
Get-AzStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0703-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d0703-105">DESCRIPTION</span></span>
<span data-ttu-id="d0703-106">**Get-AzStorageQueueStoredAccessPolicy** cmdlet 'ı, Azure depolama sırası için depolanan erişim ilkesini veya ilkelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="d0703-106">The **Get-AzStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="d0703-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d0703-107">EXAMPLES</span></span>

### <span data-ttu-id="d0703-108">Örnek 1: kuyrukta depolanan bir erişim ilkesi alma</span><span class="sxs-lookup"><span data-stu-id="d0703-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="d0703-109">Bu komut MyQueue adındaki depolama sırasındaki Policy12 adındaki erişim ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="d0703-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="d0703-110">Örnek 2: kuyruktaki tüm erişim ilkelerini sıraya alma</span><span class="sxs-lookup"><span data-stu-id="d0703-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="d0703-111">Bu komut, MyQueue adlı kuyrukta tüm depolanmış erişim ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="d0703-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="d0703-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d0703-112">PARAMETERS</span></span>

### <span data-ttu-id="d0703-113">-Context</span><span class="sxs-lookup"><span data-stu-id="d0703-113">-Context</span></span>
<span data-ttu-id="d0703-114">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0703-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="d0703-115">Depolama bağlamı edinmek için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d0703-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d0703-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0703-116">-DefaultProfile</span></span>
<span data-ttu-id="d0703-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d0703-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0703-118">-İlke</span><span class="sxs-lookup"><span data-stu-id="d0703-118">-Policy</span></span>
<span data-ttu-id="d0703-119">Bu paylaşılan erişim Imzası (SAS) belirtecinin izinlerini içeren depolanan bir erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0703-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0703-120">-Sıra</span><span class="sxs-lookup"><span data-stu-id="d0703-120">-Queue</span></span>
<span data-ttu-id="d0703-121">Azure depolama sırası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0703-121">Specifies the Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0703-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0703-122">CommonParameters</span></span>
<span data-ttu-id="d0703-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d0703-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0703-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0703-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0703-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d0703-125">INPUTS</span></span>

### <span data-ttu-id="d0703-126">System. String</span><span class="sxs-lookup"><span data-stu-id="d0703-126">System.String</span></span>

### <span data-ttu-id="d0703-127">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="d0703-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d0703-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d0703-128">OUTPUTS</span></span>

### <span data-ttu-id="d0703-129">Microsoft. Azure. Storage. Queue. SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="d0703-129">Microsoft.Azure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="d0703-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d0703-130">NOTES</span></span>

## <span data-ttu-id="d0703-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d0703-131">RELATED LINKS</span></span>

[<span data-ttu-id="d0703-132">Yeni-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d0703-132">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="d0703-133">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d0703-133">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="d0703-134">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d0703-134">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="d0703-135">Yeni-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d0703-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


