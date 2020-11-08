---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 9df25558c752b47e41bf76f7db128bd127ad0c53
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097493"
---
# <span data-ttu-id="187ef-101">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="187ef-101">Remove-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="187ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="187ef-102">SYNOPSIS</span></span>
<span data-ttu-id="187ef-103">Depolanan bir Access ilkesini Azure depolama tablosundan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="187ef-103">Removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="187ef-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="187ef-104">SYNTAX</span></span>

```
Remove-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="187ef-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="187ef-105">DESCRIPTION</span></span>
<span data-ttu-id="187ef-106">**Remove-AzStorageTableStoredAccessPolicy** cmdlet 'i Azure depolama tablosundan depolanan bir Access ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="187ef-106">The **Remove-AzStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="187ef-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="187ef-107">EXAMPLES</span></span>

### <span data-ttu-id="187ef-108">Örnek 1: depolama tablosundan depolanan bir Access ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="187ef-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="187ef-109">Bu komut, Policy05 adlı depolama tablosundan MyTable adlı ilkeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="187ef-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="187ef-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="187ef-110">PARAMETERS</span></span>

### <span data-ttu-id="187ef-111">-Context</span><span class="sxs-lookup"><span data-stu-id="187ef-111">-Context</span></span>
<span data-ttu-id="187ef-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="187ef-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="187ef-113">Depolama bağlamı edinmek için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="187ef-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="187ef-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="187ef-114">-DefaultProfile</span></span>
<span data-ttu-id="187ef-115">Azure ile iletişim.</span><span class="sxs-lookup"><span data-stu-id="187ef-115">communication with Azure.</span></span>

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

### <span data-ttu-id="187ef-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="187ef-116">-PassThru</span></span>
<span data-ttu-id="187ef-117">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="187ef-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="187ef-118">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="187ef-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="187ef-119">-İlke</span><span class="sxs-lookup"><span data-stu-id="187ef-119">-Policy</span></span>
<span data-ttu-id="187ef-120">Bu cmdlet 'in kaldırdığı depolanan erişim ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="187ef-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="187ef-121">-Tablo</span><span class="sxs-lookup"><span data-stu-id="187ef-121">-Table</span></span>
<span data-ttu-id="187ef-122">Azure tablo adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="187ef-122">Specifies the Azure table name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="187ef-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="187ef-123">-Confirm</span></span>
<span data-ttu-id="187ef-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="187ef-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="187ef-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="187ef-125">-WhatIf</span></span>
<span data-ttu-id="187ef-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="187ef-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="187ef-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="187ef-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="187ef-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="187ef-128">CommonParameters</span></span>
<span data-ttu-id="187ef-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="187ef-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="187ef-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="187ef-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="187ef-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="187ef-131">INPUTS</span></span>

### <span data-ttu-id="187ef-132">System. String</span><span class="sxs-lookup"><span data-stu-id="187ef-132">System.String</span></span>

### <span data-ttu-id="187ef-133">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="187ef-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="187ef-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="187ef-134">OUTPUTS</span></span>

### <span data-ttu-id="187ef-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="187ef-135">System.Boolean</span></span>

## <span data-ttu-id="187ef-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="187ef-136">NOTES</span></span>

## <span data-ttu-id="187ef-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="187ef-137">RELATED LINKS</span></span>

[<span data-ttu-id="187ef-138">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="187ef-138">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="187ef-139">Yeni-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="187ef-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="187ef-140">Yeni-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="187ef-140">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="187ef-141">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="187ef-141">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)
