---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: c6f0c713302ef8761c85da6d54404f86ff9fb814
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936157"
---
# <span data-ttu-id="421b4-101">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="421b4-101">Set-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="421b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="421b4-102">SYNOPSIS</span></span>
<span data-ttu-id="421b4-103">Azure depolama sırası için depolanan bir erişim ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="421b4-103">Sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="421b4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="421b4-104">SYNTAX</span></span>

```
Set-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="421b4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="421b4-105">DESCRIPTION</span></span>
<span data-ttu-id="421b4-106">**Set-AzStorageQueueStoredAccessPolicy** cmdlet 'i Azure depolama sırası için depolanan bir erişim ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="421b4-106">The **Set-AzStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="421b4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="421b4-107">EXAMPLES</span></span>

### <span data-ttu-id="421b4-108">Örnek 1: kuyrukta depolanan bir erişim ilkesini tam izinlerle ayarlama</span><span class="sxs-lookup"><span data-stu-id="421b4-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="421b4-109">Bu komut MyQueue adındaki depolama sırası için Policy07 adlı bir erişim ilkesi ayarlar.</span><span class="sxs-lookup"><span data-stu-id="421b4-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="421b4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="421b4-110">PARAMETERS</span></span>

### <span data-ttu-id="421b4-111">-Context</span><span class="sxs-lookup"><span data-stu-id="421b4-111">-Context</span></span>
<span data-ttu-id="421b4-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="421b4-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="421b4-113">Depolama bağlamı edinmek için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="421b4-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="421b4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="421b4-114">-DefaultProfile</span></span>
<span data-ttu-id="421b4-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="421b4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="421b4-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="421b4-116">-ExpiryTime</span></span>
<span data-ttu-id="421b4-117">Depolanan erişim ilkesinin geçersiz olacağı zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="421b4-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="421b4-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="421b4-118">-NoExpiryTime</span></span>
<span data-ttu-id="421b4-119">Erişim ilkesinde son kullanma tarihi olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="421b4-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="421b4-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="421b4-120">-NoStartTime</span></span>
<span data-ttu-id="421b4-121">Bu cmdlet 'in başlangıç zamanını $Null olarak ayarlamadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="421b4-121">Indicates that this cmdlet sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="421b4-122">-İzin</span><span class="sxs-lookup"><span data-stu-id="421b4-122">-Permission</span></span>
<span data-ttu-id="421b4-123">Depolanan erişim ilkesinde depolama kuyruğuna erişim izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="421b4-123">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="421b4-124">Bu dizenin `rwd` (okuma, yazma ve silme için) bir dize olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="421b4-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="421b4-125">-İlke</span><span class="sxs-lookup"><span data-stu-id="421b4-125">-Policy</span></span>
<span data-ttu-id="421b4-126">Depolanan erişim ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="421b4-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="421b4-127">-Sıra</span><span class="sxs-lookup"><span data-stu-id="421b4-127">-Queue</span></span>
<span data-ttu-id="421b4-128">Azure depolama sırası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="421b4-128">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="421b4-129">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="421b4-129">-StartTime</span></span>
<span data-ttu-id="421b4-130">Depolanan erişim ilkesinin geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="421b4-130">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="421b4-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="421b4-131">-Confirm</span></span>
<span data-ttu-id="421b4-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="421b4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="421b4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="421b4-133">-WhatIf</span></span>
<span data-ttu-id="421b4-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="421b4-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="421b4-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="421b4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="421b4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="421b4-136">CommonParameters</span></span>
<span data-ttu-id="421b4-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="421b4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="421b4-138">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="421b4-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="421b4-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="421b4-139">INPUTS</span></span>

### <span data-ttu-id="421b4-140">System. String</span><span class="sxs-lookup"><span data-stu-id="421b4-140">System.String</span></span>

### <span data-ttu-id="421b4-141">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="421b4-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="421b4-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="421b4-142">OUTPUTS</span></span>

### <span data-ttu-id="421b4-143">System. String</span><span class="sxs-lookup"><span data-stu-id="421b4-143">System.String</span></span>

## <span data-ttu-id="421b4-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="421b4-144">NOTES</span></span>

## <span data-ttu-id="421b4-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="421b4-145">RELATED LINKS</span></span>

[<span data-ttu-id="421b4-146">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="421b4-146">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="421b4-147">Yeni-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="421b4-147">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="421b4-148">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="421b4-148">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)