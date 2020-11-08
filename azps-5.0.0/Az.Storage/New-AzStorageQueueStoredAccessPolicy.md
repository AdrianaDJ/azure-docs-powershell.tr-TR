---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 65afd4039fb772d1ecf522645fe41154dae42981
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277155"
---
# <span data-ttu-id="b0c4c-101">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b0c4c-101">New-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="b0c4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0c4c-102">SYNOPSIS</span></span>
<span data-ttu-id="b0c4c-103">Azure depolama sırası için depolanan bir erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b0c4c-103">Creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="b0c4c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b0c4c-104">SYNTAX</span></span>

```
New-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0c4c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b0c4c-105">DESCRIPTION</span></span>
<span data-ttu-id="b0c4c-106">**New-AzStorageQueueStoredAccessPolicy** cmdlet 'i Azure depolama sırası için depolanan bir erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b0c4c-106">The **New-AzStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="b0c4c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b0c4c-107">EXAMPLES</span></span>

### <span data-ttu-id="b0c4c-108">Örnek 1: depolama sırasında depolanan bir erişim ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="b0c4c-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="b0c4c-109">Bu komut MyQueue adındaki depolama sırasında Policy01 adlı bir erişim ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b0c4c-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="b0c4c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b0c4c-110">PARAMETERS</span></span>

### <span data-ttu-id="b0c4c-111">-Context</span><span class="sxs-lookup"><span data-stu-id="b0c4c-111">-Context</span></span>
<span data-ttu-id="b0c4c-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b0c4c-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b0c4c-113">Depolama bağlamı edinmek için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b0c4c-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b0c4c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0c4c-114">-DefaultProfile</span></span>
<span data-ttu-id="b0c4c-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b0c4c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0c4c-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="b0c4c-116">-ExpiryTime</span></span>
<span data-ttu-id="b0c4c-117">Depolanan erişim ilkesinin geçersiz olacağı zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="b0c4c-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="b0c4c-118">-İzin</span><span class="sxs-lookup"><span data-stu-id="b0c4c-118">-Permission</span></span>
<span data-ttu-id="b0c4c-119">Depolanan erişim ilkesinde depolama kuyruğuna erişim izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b0c4c-119">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="b0c4c-120">Bu dizenin `rwd` (okuma, yazma ve silme için) bir dize olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="b0c4c-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="b0c4c-121">-İlke</span><span class="sxs-lookup"><span data-stu-id="b0c4c-121">-Policy</span></span>
<span data-ttu-id="b0c4c-122">Depolanan erişim ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b0c4c-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="b0c4c-123">-Sıra</span><span class="sxs-lookup"><span data-stu-id="b0c4c-123">-Queue</span></span>
<span data-ttu-id="b0c4c-124">Azure depolama sırası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b0c4c-124">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="b0c4c-125">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="b0c4c-125">-StartTime</span></span>
<span data-ttu-id="b0c4c-126">Depolanan erişim ilkesinin geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="b0c4c-126">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="b0c4c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0c4c-127">CommonParameters</span></span>
<span data-ttu-id="b0c4c-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b0c4c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0c4c-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0c4c-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0c4c-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b0c4c-130">INPUTS</span></span>

### <span data-ttu-id="b0c4c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b0c4c-131">System.String</span></span>

### <span data-ttu-id="b0c4c-132">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="b0c4c-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b0c4c-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b0c4c-133">OUTPUTS</span></span>

### <span data-ttu-id="b0c4c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b0c4c-134">System.String</span></span>

## <span data-ttu-id="b0c4c-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b0c4c-135">NOTES</span></span>

## <span data-ttu-id="b0c4c-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b0c4c-136">RELATED LINKS</span></span>

[<span data-ttu-id="b0c4c-137">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b0c4c-137">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="b0c4c-138">Yeni-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b0c4c-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="b0c4c-139">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b0c4c-139">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="b0c4c-140">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b0c4c-140">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)


