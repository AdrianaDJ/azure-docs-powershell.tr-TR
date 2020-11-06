---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageQueueStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 69ec2307dfdf8525f892720281079c58c1e1bd55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593870"
---
# <span data-ttu-id="770c3-101">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="770c3-101">Set-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="770c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="770c3-102">SYNOPSIS</span></span>
<span data-ttu-id="770c3-103">Azure depolama sırası için depolanan bir erişim ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="770c3-103">Sets a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="770c3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="770c3-104">SYNTAX</span></span>

```
Set-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="770c3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="770c3-105">DESCRIPTION</span></span>
<span data-ttu-id="770c3-106">**Set-AzureStorageQueueStoredAccessPolicy** cmdlet 'i Azure depolama sırası için depolanan bir erişim ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="770c3-106">The **Set-AzureStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="770c3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="770c3-107">EXAMPLES</span></span>

### <span data-ttu-id="770c3-108">Örnek 1: kuyrukta depolanan bir erişim ilkesini tam izinlerle ayarlama</span><span class="sxs-lookup"><span data-stu-id="770c3-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="770c3-109">Bu komut MyQueue adındaki depolama sırası için Policy07 adlı bir erişim ilkesi ayarlar.</span><span class="sxs-lookup"><span data-stu-id="770c3-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="770c3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="770c3-110">PARAMETERS</span></span>

### <span data-ttu-id="770c3-111">-Context</span><span class="sxs-lookup"><span data-stu-id="770c3-111">-Context</span></span>
<span data-ttu-id="770c3-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="770c3-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="770c3-113">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="770c3-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="770c3-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="770c3-114">-ExpiryTime</span></span>
<span data-ttu-id="770c3-115">Depolanan erişim ilkesinin geçersiz olacağı zamanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="770c3-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="770c3-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="770c3-116">-NoExpiryTime</span></span>
<span data-ttu-id="770c3-117">Erişim ilkesinde son kullanma tarihi olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="770c3-117">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="770c3-118">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="770c3-118">-NoStartTime</span></span>
<span data-ttu-id="770c3-119">Bu cmdlet 'in başlangıç zamanını $Null olarak ayarlamadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="770c3-119">Indicates that this cmdlet sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="770c3-120">-İzin</span><span class="sxs-lookup"><span data-stu-id="770c3-120">-Permission</span></span>
<span data-ttu-id="770c3-121">Depolanan erişim ilkesinde depolama kuyruğuna erişim izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="770c3-121">Specifies permissions in the stored access policy to access the storage queue.</span></span>

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

### <span data-ttu-id="770c3-122">-İlke</span><span class="sxs-lookup"><span data-stu-id="770c3-122">-Policy</span></span>
<span data-ttu-id="770c3-123">Depolanan erişim ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="770c3-123">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="770c3-124">-Sıra</span><span class="sxs-lookup"><span data-stu-id="770c3-124">-Queue</span></span>
<span data-ttu-id="770c3-125">Azure depolama sırası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="770c3-125">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="770c3-126">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="770c3-126">-StartTime</span></span>
<span data-ttu-id="770c3-127">Depolanan erişim ilkesinin geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="770c3-127">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="770c3-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="770c3-128">-Confirm</span></span>
<span data-ttu-id="770c3-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="770c3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="770c3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="770c3-130">-WhatIf</span></span>
<span data-ttu-id="770c3-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="770c3-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="770c3-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="770c3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="770c3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="770c3-133">CommonParameters</span></span>
<span data-ttu-id="770c3-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="770c3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="770c3-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="770c3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="770c3-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="770c3-136">INPUTS</span></span>

### <span data-ttu-id="770c3-137">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="770c3-137">IStorageContext</span></span>

<span data-ttu-id="770c3-138">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="770c3-138">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="770c3-139">Dizisi</span><span class="sxs-lookup"><span data-stu-id="770c3-139">String</span></span>

<span data-ttu-id="770c3-140">' Queue ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="770c3-140">Parameter 'Queue' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="770c3-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="770c3-141">OUTPUTS</span></span>

### <span data-ttu-id="770c3-142">System. String</span><span class="sxs-lookup"><span data-stu-id="770c3-142">System.String</span></span>

## <span data-ttu-id="770c3-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="770c3-143">NOTES</span></span>

## <span data-ttu-id="770c3-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="770c3-144">RELATED LINKS</span></span>

[<span data-ttu-id="770c3-145">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="770c3-145">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="770c3-146">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="770c3-146">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="770c3-147">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="770c3-147">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)
