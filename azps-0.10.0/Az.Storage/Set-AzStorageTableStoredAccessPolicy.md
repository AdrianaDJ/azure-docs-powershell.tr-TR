---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: fe98eee14797ff26c39b003d8ab1c9826c8ec687
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936149"
---
# <span data-ttu-id="913f6-101">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="913f6-101">Set-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="913f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="913f6-102">SYNOPSIS</span></span>
<span data-ttu-id="913f6-103">Azure depolama tablosu için depolanan erişim ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="913f6-103">Sets the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="913f6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="913f6-104">SYNTAX</span></span>

```
Set-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="913f6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="913f6-105">DESCRIPTION</span></span>
<span data-ttu-id="913f6-106">**Set-AzStorageTableStoredAccessPolicy** cmdlet 'i Azure depolama tablosu için depolanan erişim ilkesini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="913f6-106">The **Set-AzStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="913f6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="913f6-107">EXAMPLES</span></span>

### <span data-ttu-id="913f6-108">Örnek 1: tüm izinle tabloda depolanan bir erişim ilkesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="913f6-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08" -Permission raud
```

<span data-ttu-id="913f6-109">Bu komut, MyTable adlı depolama tablosu için Policy08 adındaki bir erişim ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="913f6-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="913f6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="913f6-110">PARAMETERS</span></span>

### <span data-ttu-id="913f6-111">-Context</span><span class="sxs-lookup"><span data-stu-id="913f6-111">-Context</span></span>
<span data-ttu-id="913f6-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="913f6-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="913f6-113">Depolama bağlamı edinmek için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="913f6-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="913f6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="913f6-114">-DefaultProfile</span></span>
<span data-ttu-id="913f6-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="913f6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="913f6-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="913f6-116">-ExpiryTime</span></span>
<span data-ttu-id="913f6-117">Depolanan erişim ilkesinin zaman dolacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="913f6-117">Specifies the time at which the stored access policy expires.</span></span>

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

### <span data-ttu-id="913f6-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="913f6-118">-NoExpiryTime</span></span>
<span data-ttu-id="913f6-119">Erişim ilkesinde son kullanma tarihi olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="913f6-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="913f6-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="913f6-120">-NoStartTime</span></span>
<span data-ttu-id="913f6-121">Başlangıç zamanının $Null olarak ayarlandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="913f6-121">Indicates that the start time is set to $Null.</span></span>

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

### <span data-ttu-id="913f6-122">-İzin</span><span class="sxs-lookup"><span data-stu-id="913f6-122">-Permission</span></span>
<span data-ttu-id="913f6-123">Depolanan erişim ilkesinde depolama tablosuna erişim izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="913f6-123">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="913f6-124">Bu dizenin `rwd` (okuma, yazma ve silme için) bir dize olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="913f6-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="913f6-125">-İlke</span><span class="sxs-lookup"><span data-stu-id="913f6-125">-Policy</span></span>
<span data-ttu-id="913f6-126">Depolanan erişim ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="913f6-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="913f6-127">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="913f6-127">-StartTime</span></span>
<span data-ttu-id="913f6-128">Depolanan erişim ilkesinin geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="913f6-128">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="913f6-129">-Tablo</span><span class="sxs-lookup"><span data-stu-id="913f6-129">-Table</span></span>
<span data-ttu-id="913f6-130">Azure depolama tablosu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="913f6-130">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="913f6-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="913f6-131">-Confirm</span></span>
<span data-ttu-id="913f6-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="913f6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="913f6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="913f6-133">-WhatIf</span></span>
<span data-ttu-id="913f6-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="913f6-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="913f6-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="913f6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="913f6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="913f6-136">CommonParameters</span></span>
<span data-ttu-id="913f6-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="913f6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="913f6-138">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="913f6-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="913f6-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="913f6-139">INPUTS</span></span>

### <span data-ttu-id="913f6-140">System. String</span><span class="sxs-lookup"><span data-stu-id="913f6-140">System.String</span></span>

### <span data-ttu-id="913f6-141">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="913f6-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="913f6-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="913f6-142">OUTPUTS</span></span>

### <span data-ttu-id="913f6-143">System. String</span><span class="sxs-lookup"><span data-stu-id="913f6-143">System.String</span></span>

## <span data-ttu-id="913f6-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="913f6-144">NOTES</span></span>

## <span data-ttu-id="913f6-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="913f6-145">RELATED LINKS</span></span>

[<span data-ttu-id="913f6-146">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="913f6-146">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="913f6-147">Yeni-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="913f6-147">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="913f6-148">Yeni-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="913f6-148">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="913f6-149">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="913f6-149">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)
