---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 9ef4be8331c1de38789d25903db9e98f4e2d8cd1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939011"
---
# <span data-ttu-id="5b87e-101">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5b87e-101">Get-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="5b87e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b87e-102">SYNOPSIS</span></span>
<span data-ttu-id="5b87e-103">Depolanan erişim ilkesini veya bir Azure depolama sırasının ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="5b87e-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b87e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5b87e-104">SYNTAX</span></span>

```
Get-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b87e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5b87e-105">DESCRIPTION</span></span>
<span data-ttu-id="5b87e-106">**Get-AzureStorageQueueStoredAccessPolicy** cmdlet 'i Azure depolama sırası için depolanan erişim ilkesini veya ilkelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="5b87e-106">The **Get-AzureStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="5b87e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5b87e-107">EXAMPLES</span></span>

### <span data-ttu-id="5b87e-108">Örnek 1: kuyrukta depolanan bir erişim ilkesi alma</span><span class="sxs-lookup"><span data-stu-id="5b87e-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="5b87e-109">Bu komut MyQueue adındaki depolama sırasındaki Policy12 adındaki erişim ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="5b87e-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="5b87e-110">Örnek 2: kuyruktaki tüm erişim ilkelerini sıraya alma</span><span class="sxs-lookup"><span data-stu-id="5b87e-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="5b87e-111">Bu komut, MyQueue adlı kuyrukta tüm depolanmış erişim ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="5b87e-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="5b87e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5b87e-112">PARAMETERS</span></span>

### <span data-ttu-id="5b87e-113">-Context</span><span class="sxs-lookup"><span data-stu-id="5b87e-113">-Context</span></span>
<span data-ttu-id="5b87e-114">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b87e-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="5b87e-115">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5b87e-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="5b87e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b87e-116">-DefaultProfile</span></span>
<span data-ttu-id="5b87e-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5b87e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b87e-118">-İlke</span><span class="sxs-lookup"><span data-stu-id="5b87e-118">-Policy</span></span>
<span data-ttu-id="5b87e-119">Bu paylaşılan erişim Imzası (SAS) belirtecinin izinlerini içeren depolanan bir erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b87e-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="5b87e-120">-Sıra</span><span class="sxs-lookup"><span data-stu-id="5b87e-120">-Queue</span></span>
<span data-ttu-id="5b87e-121">Azure depolama sırası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b87e-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="5b87e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b87e-122">CommonParameters</span></span>
<span data-ttu-id="5b87e-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5b87e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b87e-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b87e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b87e-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5b87e-125">INPUTS</span></span>

### <span data-ttu-id="5b87e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="5b87e-126">System.String</span></span>

### <span data-ttu-id="5b87e-127">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="5b87e-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5b87e-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5b87e-128">OUTPUTS</span></span>

### <span data-ttu-id="5b87e-129">Microsoft. Windowsazde. Storage. Queue. SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="5b87e-129">Microsoft.WindowsAzure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="5b87e-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5b87e-130">NOTES</span></span>

## <span data-ttu-id="5b87e-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5b87e-131">RELATED LINKS</span></span>

[<span data-ttu-id="5b87e-132">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5b87e-132">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="5b87e-133">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5b87e-133">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="5b87e-134">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5b87e-134">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="5b87e-135">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="5b87e-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


