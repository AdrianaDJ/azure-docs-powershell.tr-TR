---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragetablestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 4d28b17146e7c4a4f4a87081b0577786b4b39930
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940199"
---
# <span data-ttu-id="411e3-101">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="411e3-101">Set-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="411e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="411e3-102">SYNOPSIS</span></span>
<span data-ttu-id="411e3-103">Azure depolama tablosu için depolanan erişim ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="411e3-103">Sets the stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="411e3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="411e3-104">SYNTAX</span></span>

```
Set-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="411e3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="411e3-105">DESCRIPTION</span></span>
<span data-ttu-id="411e3-106">**Set-AzureStorageTableStoredAccessPolicy** cmdlet 'ı bir Azure depolama tablosu için depolanan erişim ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="411e3-106">The **Set-AzureStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="411e3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="411e3-107">EXAMPLES</span></span>

### <span data-ttu-id="411e3-108">Örnek 1: tüm izinle tabloda depolanan bir erişim ilkesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="411e3-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08" -Permission raud
```

<span data-ttu-id="411e3-109">Bu komut, MyTable adlı depolama tablosu için Policy08 adındaki bir erişim ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="411e3-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="411e3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="411e3-110">PARAMETERS</span></span>

### <span data-ttu-id="411e3-111">-Context</span><span class="sxs-lookup"><span data-stu-id="411e3-111">-Context</span></span>
<span data-ttu-id="411e3-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="411e3-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="411e3-113">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="411e3-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="411e3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="411e3-114">-DefaultProfile</span></span>
<span data-ttu-id="411e3-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="411e3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="411e3-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="411e3-116">-ExpiryTime</span></span>
<span data-ttu-id="411e3-117">Depolanan erişim ilkesinin zaman dolacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="411e3-117">Specifies the time at which the stored access policy expires.</span></span>

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

### <span data-ttu-id="411e3-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="411e3-118">-NoExpiryTime</span></span>
<span data-ttu-id="411e3-119">Erişim ilkesinde son kullanma tarihi olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="411e3-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="411e3-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="411e3-120">-NoStartTime</span></span>
<span data-ttu-id="411e3-121">Başlangıç zamanının $Null olarak ayarlandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="411e3-121">Indicates that the start time is set to $Null.</span></span>

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

### <span data-ttu-id="411e3-122">-İzin</span><span class="sxs-lookup"><span data-stu-id="411e3-122">-Permission</span></span>
<span data-ttu-id="411e3-123">Depolanan erişim ilkesinde depolama tablosuna erişim izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="411e3-123">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="411e3-124">Bu dizenin `rwd` (okuma, yazma ve silme için) bir dize olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="411e3-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="411e3-125">-İlke</span><span class="sxs-lookup"><span data-stu-id="411e3-125">-Policy</span></span>
<span data-ttu-id="411e3-126">Depolanan erişim ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="411e3-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="411e3-127">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="411e3-127">-StartTime</span></span>
<span data-ttu-id="411e3-128">Depolanan erişim ilkesinin geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="411e3-128">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="411e3-129">-Tablo</span><span class="sxs-lookup"><span data-stu-id="411e3-129">-Table</span></span>
<span data-ttu-id="411e3-130">Azure depolama tablosu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="411e3-130">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="411e3-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="411e3-131">-Confirm</span></span>
<span data-ttu-id="411e3-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="411e3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="411e3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="411e3-133">-WhatIf</span></span>
<span data-ttu-id="411e3-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="411e3-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="411e3-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="411e3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="411e3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="411e3-136">CommonParameters</span></span>
<span data-ttu-id="411e3-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="411e3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="411e3-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="411e3-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="411e3-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="411e3-139">INPUTS</span></span>

### <span data-ttu-id="411e3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="411e3-140">System.String</span></span>

### <span data-ttu-id="411e3-141">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="411e3-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="411e3-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="411e3-142">OUTPUTS</span></span>

### <span data-ttu-id="411e3-143">System. String</span><span class="sxs-lookup"><span data-stu-id="411e3-143">System.String</span></span>

## <span data-ttu-id="411e3-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="411e3-144">NOTES</span></span>

## <span data-ttu-id="411e3-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="411e3-145">RELATED LINKS</span></span>

[<span data-ttu-id="411e3-146">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="411e3-146">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="411e3-147">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="411e3-147">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="411e3-148">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="411e3-148">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="411e3-149">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="411e3-149">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)
