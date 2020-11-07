---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 9a3a19b2e0773d1513ce57dc5fe7ca7502bb325d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765133"
---
# <span data-ttu-id="e6213-101">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e6213-101">Set-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="e6213-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6213-102">SYNOPSIS</span></span>
<span data-ttu-id="e6213-103">Azure depolama sırası için depolanan bir erişim ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e6213-103">Sets a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6213-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e6213-104">SYNTAX</span></span>

```
Set-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6213-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e6213-105">DESCRIPTION</span></span>
<span data-ttu-id="e6213-106">**Set-AzureStorageQueueStoredAccessPolicy** cmdlet 'i Azure depolama sırası için depolanan bir erişim ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e6213-106">The **Set-AzureStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="e6213-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e6213-107">EXAMPLES</span></span>

### <span data-ttu-id="e6213-108">Örnek 1: kuyrukta depolanan bir erişim ilkesini tam izinlerle ayarlama</span><span class="sxs-lookup"><span data-stu-id="e6213-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="e6213-109">Bu komut MyQueue adındaki depolama sırası için Policy07 adlı bir erişim ilkesi ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e6213-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="e6213-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e6213-110">PARAMETERS</span></span>

### <span data-ttu-id="e6213-111">-Context</span><span class="sxs-lookup"><span data-stu-id="e6213-111">-Context</span></span>
<span data-ttu-id="e6213-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6213-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e6213-113">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e6213-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e6213-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="e6213-114">-ExpiryTime</span></span>
<span data-ttu-id="e6213-115">Depolanan erişim ilkesinin geçersiz olacağı zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6213-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6213-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="e6213-116">-NoExpiryTime</span></span>
<span data-ttu-id="e6213-117">Erişim ilkesinde son kullanma tarihi olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e6213-117">Indicates that the access policy has no expiration date.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6213-118">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="e6213-118">-NoStartTime</span></span>
<span data-ttu-id="e6213-119">Bu cmdlet 'in başlangıç zamanını $Null olarak ayarlamadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e6213-119">Indicates that this cmdlet sets the start time to be $Null.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6213-120">-İzin</span><span class="sxs-lookup"><span data-stu-id="e6213-120">-Permission</span></span>
<span data-ttu-id="e6213-121">Depolanan erişim ilkesinde depolama kuyruğuna erişim izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6213-121">Specifies permissions in the stored access policy to access the storage queue.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6213-122">-İlke</span><span class="sxs-lookup"><span data-stu-id="e6213-122">-Policy</span></span>
<span data-ttu-id="e6213-123">Depolanan erişim ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6213-123">Specifies the name for the stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6213-124">-Sıra</span><span class="sxs-lookup"><span data-stu-id="e6213-124">-Queue</span></span>
<span data-ttu-id="e6213-125">Azure depolama sırası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6213-125">Specifies the Azure storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6213-126">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="e6213-126">-StartTime</span></span>
<span data-ttu-id="e6213-127">Depolanan erişim ilkesinin geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6213-127">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6213-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="e6213-128">-Confirm</span></span>
<span data-ttu-id="e6213-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e6213-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6213-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6213-130">-WhatIf</span></span>
<span data-ttu-id="e6213-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e6213-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6213-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e6213-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6213-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6213-133">CommonParameters</span></span>
<span data-ttu-id="e6213-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e6213-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6213-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6213-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6213-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e6213-136">INPUTS</span></span>

### <span data-ttu-id="e6213-137">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="e6213-137">IStorageContext</span></span>

<span data-ttu-id="e6213-138">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="e6213-138">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="e6213-139">Dizisi</span><span class="sxs-lookup"><span data-stu-id="e6213-139">String</span></span>

<span data-ttu-id="e6213-140">' Queue ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="e6213-140">Parameter 'Queue' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="e6213-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e6213-141">OUTPUTS</span></span>

### <span data-ttu-id="e6213-142">System. String</span><span class="sxs-lookup"><span data-stu-id="e6213-142">System.String</span></span>

## <span data-ttu-id="e6213-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e6213-143">NOTES</span></span>

## <span data-ttu-id="e6213-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e6213-144">RELATED LINKS</span></span>

[<span data-ttu-id="e6213-145">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e6213-145">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="e6213-146">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e6213-146">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="e6213-147">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e6213-147">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)
