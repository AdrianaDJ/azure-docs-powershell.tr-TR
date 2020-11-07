---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 4e1b58e2ca2586ada574b55a03287d1cc5915b6f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940211"
---
# <span data-ttu-id="a0b0b-101">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a0b0b-101">Set-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="a0b0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0b0b-102">SYNOPSIS</span></span>
<span data-ttu-id="a0b0b-103">Azure depolama sırası için depolanan bir erişim ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a0b0b-103">Sets a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0b0b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a0b0b-104">SYNTAX</span></span>

```
Set-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0b0b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a0b0b-105">DESCRIPTION</span></span>
<span data-ttu-id="a0b0b-106">**Set-AzureStorageQueueStoredAccessPolicy** cmdlet 'i Azure depolama sırası için depolanan bir erişim ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a0b0b-106">The **Set-AzureStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="a0b0b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a0b0b-107">EXAMPLES</span></span>

### <span data-ttu-id="a0b0b-108">Örnek 1: kuyrukta depolanan bir erişim ilkesini tam izinlerle ayarlama</span><span class="sxs-lookup"><span data-stu-id="a0b0b-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="a0b0b-109">Bu komut MyQueue adındaki depolama sırası için Policy07 adlı bir erişim ilkesi ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a0b0b-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="a0b0b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a0b0b-110">PARAMETERS</span></span>

### <span data-ttu-id="a0b0b-111">-Context</span><span class="sxs-lookup"><span data-stu-id="a0b0b-111">-Context</span></span>
<span data-ttu-id="a0b0b-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0b0b-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a0b0b-113">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a0b0b-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a0b0b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0b0b-114">-DefaultProfile</span></span>
<span data-ttu-id="a0b0b-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a0b0b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0b0b-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="a0b0b-116">-ExpiryTime</span></span>
<span data-ttu-id="a0b0b-117">Depolanan erişim ilkesinin geçersiz olacağı zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0b0b-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="a0b0b-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="a0b0b-118">-NoExpiryTime</span></span>
<span data-ttu-id="a0b0b-119">Erişim ilkesinde son kullanma tarihi olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a0b0b-119">Indicates that the access policy has no expiration date.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0b0b-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="a0b0b-120">-NoStartTime</span></span>
<span data-ttu-id="a0b0b-121">Bu cmdlet 'in başlangıç zamanını $Null olarak ayarlamadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a0b0b-121">Indicates that this cmdlet sets the start time to be $Null.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0b0b-122">-İzin</span><span class="sxs-lookup"><span data-stu-id="a0b0b-122">-Permission</span></span>
<span data-ttu-id="a0b0b-123">Depolanan erişim ilkesinde depolama kuyruğuna erişim izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0b0b-123">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="a0b0b-124">Bu dizenin `rwd` (okuma, yazma ve silme için) bir dize olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="a0b0b-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="a0b0b-125">-İlke</span><span class="sxs-lookup"><span data-stu-id="a0b0b-125">-Policy</span></span>
<span data-ttu-id="a0b0b-126">Depolanan erişim ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0b0b-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="a0b0b-127">-Sıra</span><span class="sxs-lookup"><span data-stu-id="a0b0b-127">-Queue</span></span>
<span data-ttu-id="a0b0b-128">Azure depolama sırası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0b0b-128">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="a0b0b-129">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="a0b0b-129">-StartTime</span></span>
<span data-ttu-id="a0b0b-130">Depolanan erişim ilkesinin geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0b0b-130">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="a0b0b-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="a0b0b-131">-Confirm</span></span>
<span data-ttu-id="a0b0b-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a0b0b-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0b0b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0b0b-133">-WhatIf</span></span>
<span data-ttu-id="a0b0b-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a0b0b-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0b0b-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a0b0b-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0b0b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0b0b-136">CommonParameters</span></span>
<span data-ttu-id="a0b0b-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a0b0b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0b0b-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0b0b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0b0b-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a0b0b-139">INPUTS</span></span>

### <span data-ttu-id="a0b0b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a0b0b-140">System.String</span></span>

### <span data-ttu-id="a0b0b-141">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="a0b0b-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a0b0b-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a0b0b-142">OUTPUTS</span></span>

### <span data-ttu-id="a0b0b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="a0b0b-143">System.String</span></span>

## <span data-ttu-id="a0b0b-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a0b0b-144">NOTES</span></span>

## <span data-ttu-id="a0b0b-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a0b0b-145">RELATED LINKS</span></span>

[<span data-ttu-id="a0b0b-146">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a0b0b-146">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="a0b0b-147">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a0b0b-147">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="a0b0b-148">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a0b0b-148">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)
