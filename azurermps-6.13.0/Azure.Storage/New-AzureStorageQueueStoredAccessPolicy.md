---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: ea317e4fba3a1c92b55a4cab1acb46873b1d5c92
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591508"
---
# <span data-ttu-id="18eb1-101">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="18eb1-101">New-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="18eb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18eb1-102">SYNOPSIS</span></span>
<span data-ttu-id="18eb1-103">Azure depolama sırası için depolanan bir erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="18eb1-103">Creates a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18eb1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="18eb1-104">SYNTAX</span></span>

```
New-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18eb1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="18eb1-105">DESCRIPTION</span></span>
<span data-ttu-id="18eb1-106">**New-AzureStorageQueueStoredAccessPolicy** cmdlet 'i Azure depolama sırası için depolanan bir erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="18eb1-106">The **New-AzureStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="18eb1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="18eb1-107">EXAMPLES</span></span>

### <span data-ttu-id="18eb1-108">Örnek 1: depolama sırasında depolanan bir erişim ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="18eb1-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="18eb1-109">Bu komut MyQueue adındaki depolama sırasında Policy01 adlı bir erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="18eb1-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="18eb1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="18eb1-110">PARAMETERS</span></span>

### <span data-ttu-id="18eb1-111">-Context</span><span class="sxs-lookup"><span data-stu-id="18eb1-111">-Context</span></span>
<span data-ttu-id="18eb1-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="18eb1-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="18eb1-113">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="18eb1-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="18eb1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18eb1-114">-DefaultProfile</span></span>
<span data-ttu-id="18eb1-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="18eb1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18eb1-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="18eb1-116">-ExpiryTime</span></span>
<span data-ttu-id="18eb1-117">Depolanan erişim ilkesinin geçersiz olacağı zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="18eb1-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18eb1-118">-İzin</span><span class="sxs-lookup"><span data-stu-id="18eb1-118">-Permission</span></span>
<span data-ttu-id="18eb1-119">Depolanan erişim ilkesinde depolama kuyruğuna erişim izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="18eb1-119">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="18eb1-120">Bu dizenin `rwd` (okuma, yazma ve silme için) bir dize olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="18eb1-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18eb1-121">-İlke</span><span class="sxs-lookup"><span data-stu-id="18eb1-121">-Policy</span></span>
<span data-ttu-id="18eb1-122">Depolanan erişim ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="18eb1-122">Specifies a name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18eb1-123">-Sıra</span><span class="sxs-lookup"><span data-stu-id="18eb1-123">-Queue</span></span>
<span data-ttu-id="18eb1-124">Azure depolama sırası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="18eb1-124">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="18eb1-125">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="18eb1-125">-StartTime</span></span>
<span data-ttu-id="18eb1-126">Depolanan erişim ilkesinin geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="18eb1-126">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18eb1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18eb1-127">CommonParameters</span></span>
<span data-ttu-id="18eb1-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="18eb1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18eb1-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18eb1-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18eb1-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="18eb1-130">INPUTS</span></span>

### <span data-ttu-id="18eb1-131">System. String</span><span class="sxs-lookup"><span data-stu-id="18eb1-131">System.String</span></span>

### <span data-ttu-id="18eb1-132">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="18eb1-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="18eb1-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="18eb1-133">OUTPUTS</span></span>

### <span data-ttu-id="18eb1-134">System. String</span><span class="sxs-lookup"><span data-stu-id="18eb1-134">System.String</span></span>

## <span data-ttu-id="18eb1-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="18eb1-135">NOTES</span></span>

## <span data-ttu-id="18eb1-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="18eb1-136">RELATED LINKS</span></span>

[<span data-ttu-id="18eb1-137">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="18eb1-137">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="18eb1-138">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="18eb1-138">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="18eb1-139">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="18eb1-139">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="18eb1-140">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="18eb1-140">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)


