---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 822781f6c46eeb76a953eaa66935c03cd76df737
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096992"
---
# <span data-ttu-id="1c9e4-101">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1c9e4-101">Set-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="1c9e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c9e4-102">SYNOPSIS</span></span>
<span data-ttu-id="1c9e4-103">Azure depolama tablosu için depolanan erişim ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-103">Sets the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="1c9e4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1c9e4-104">SYNTAX</span></span>

```
Set-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c9e4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1c9e4-105">DESCRIPTION</span></span>
<span data-ttu-id="1c9e4-106">**Set-AzStorageTableStoredAccessPolicy** cmdlet 'i Azure depolama tablosu için depolanan erişim ilkesini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-106">The **Set-AzStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="1c9e4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1c9e4-107">EXAMPLES</span></span>

### <span data-ttu-id="1c9e4-108">Örnek 1: tüm izinle tabloda depolanan bir erişim ilkesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="1c9e4-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08" -Permission raud
```

<span data-ttu-id="1c9e4-109">Bu komut, MyTable adlı depolama tablosu için Policy08 adındaki bir erişim ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="1c9e4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1c9e4-110">PARAMETERS</span></span>

### <span data-ttu-id="1c9e4-111">-Context</span><span class="sxs-lookup"><span data-stu-id="1c9e4-111">-Context</span></span>
<span data-ttu-id="1c9e4-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="1c9e4-113">Depolama bağlamı edinmek için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="1c9e4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c9e4-114">-DefaultProfile</span></span>
<span data-ttu-id="1c9e4-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c9e4-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="1c9e4-116">-ExpiryTime</span></span>
<span data-ttu-id="1c9e4-117">Depolanan erişim ilkesinin zaman dolacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-117">Specifies the time at which the stored access policy expires.</span></span>

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

### <span data-ttu-id="1c9e4-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="1c9e4-118">-NoExpiryTime</span></span>
<span data-ttu-id="1c9e4-119">Erişim ilkesinde son kullanma tarihi olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="1c9e4-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="1c9e4-120">-NoStartTime</span></span>
<span data-ttu-id="1c9e4-121">Başlangıç zamanının $Null olarak ayarlandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-121">Indicates that the start time is set to $Null.</span></span>

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

### <span data-ttu-id="1c9e4-122">-İzin</span><span class="sxs-lookup"><span data-stu-id="1c9e4-122">-Permission</span></span>
<span data-ttu-id="1c9e4-123">Depolanan erişim ilkesinde depolama tablosuna erişim izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-123">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="1c9e4-124">Bu dizenin `rwd` (okuma, yazma ve silme için) bir dize olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="1c9e4-125">-İlke</span><span class="sxs-lookup"><span data-stu-id="1c9e4-125">-Policy</span></span>
<span data-ttu-id="1c9e4-126">Depolanan erişim ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="1c9e4-127">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="1c9e4-127">-StartTime</span></span>
<span data-ttu-id="1c9e4-128">Depolanan erişim ilkesinin geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-128">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="1c9e4-129">-Tablo</span><span class="sxs-lookup"><span data-stu-id="1c9e4-129">-Table</span></span>
<span data-ttu-id="1c9e4-130">Azure depolama tablosu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-130">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="1c9e4-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="1c9e4-131">-Confirm</span></span>
<span data-ttu-id="1c9e4-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c9e4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c9e4-133">-WhatIf</span></span>
<span data-ttu-id="1c9e4-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1c9e4-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c9e4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c9e4-136">CommonParameters</span></span>
<span data-ttu-id="1c9e4-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1c9e4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c9e4-138">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c9e4-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c9e4-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1c9e4-139">INPUTS</span></span>

### <span data-ttu-id="1c9e4-140">System. String</span><span class="sxs-lookup"><span data-stu-id="1c9e4-140">System.String</span></span>

### <span data-ttu-id="1c9e4-141">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="1c9e4-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1c9e4-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1c9e4-142">OUTPUTS</span></span>

### <span data-ttu-id="1c9e4-143">System. String</span><span class="sxs-lookup"><span data-stu-id="1c9e4-143">System.String</span></span>

## <span data-ttu-id="1c9e4-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1c9e4-144">NOTES</span></span>

## <span data-ttu-id="1c9e4-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1c9e4-145">RELATED LINKS</span></span>

[<span data-ttu-id="1c9e4-146">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1c9e4-146">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="1c9e4-147">Yeni-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="1c9e4-147">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="1c9e4-148">Yeni-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1c9e4-148">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="1c9e4-149">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1c9e4-149">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)