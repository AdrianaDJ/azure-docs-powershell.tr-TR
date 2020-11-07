---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragetablestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 6d32ddf53f675f2ab2897e4bb9ec85655e0fcd14
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939966"
---
# <span data-ttu-id="3cacb-101">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3cacb-101">Remove-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="3cacb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cacb-102">SYNOPSIS</span></span>
<span data-ttu-id="3cacb-103">Depolanan bir Access ilkesini Azure depolama tablosundan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3cacb-103">Removes a stored access policy from an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3cacb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3cacb-104">SYNTAX</span></span>

```
Remove-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3cacb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3cacb-105">DESCRIPTION</span></span>
<span data-ttu-id="3cacb-106">**Remove-AzureStorageTableStoredAccessPolicy** cmdlet 'i Azure depolama tablosundan depolanan bir Access ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3cacb-106">The **Remove-AzureStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="3cacb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3cacb-107">EXAMPLES</span></span>

### <span data-ttu-id="3cacb-108">Örnek 1: depolama tablosundan depolanan bir Access ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="3cacb-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="3cacb-109">Bu komut, Policy05 adlı depolama tablosundan MyTable adlı ilkeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3cacb-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="3cacb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3cacb-110">PARAMETERS</span></span>

### <span data-ttu-id="3cacb-111">-Context</span><span class="sxs-lookup"><span data-stu-id="3cacb-111">-Context</span></span>
<span data-ttu-id="3cacb-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3cacb-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3cacb-113">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3cacb-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3cacb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cacb-114">-DefaultProfile</span></span>
<span data-ttu-id="3cacb-115">Azure ile iletişim.</span><span class="sxs-lookup"><span data-stu-id="3cacb-115">communication with Azure.</span></span>

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

### <span data-ttu-id="3cacb-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3cacb-116">-PassThru</span></span>
<span data-ttu-id="3cacb-117">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="3cacb-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="3cacb-118">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="3cacb-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="3cacb-119">-İlke</span><span class="sxs-lookup"><span data-stu-id="3cacb-119">-Policy</span></span>
<span data-ttu-id="3cacb-120">Bu cmdlet 'in kaldırdığı depolanan erişim ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3cacb-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3cacb-121">-Tablo</span><span class="sxs-lookup"><span data-stu-id="3cacb-121">-Table</span></span>
<span data-ttu-id="3cacb-122">Azure tablo adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3cacb-122">Specifies the Azure table name.</span></span>

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

### <span data-ttu-id="3cacb-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="3cacb-123">-Confirm</span></span>
<span data-ttu-id="3cacb-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3cacb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cacb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cacb-125">-WhatIf</span></span>
<span data-ttu-id="3cacb-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3cacb-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cacb-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3cacb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cacb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cacb-128">CommonParameters</span></span>
<span data-ttu-id="3cacb-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3cacb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cacb-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cacb-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cacb-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3cacb-131">INPUTS</span></span>

### <span data-ttu-id="3cacb-132">System. String</span><span class="sxs-lookup"><span data-stu-id="3cacb-132">System.String</span></span>

### <span data-ttu-id="3cacb-133">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="3cacb-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3cacb-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3cacb-134">OUTPUTS</span></span>

### <span data-ttu-id="3cacb-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3cacb-135">System.Boolean</span></span>

## <span data-ttu-id="3cacb-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3cacb-136">NOTES</span></span>

## <span data-ttu-id="3cacb-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3cacb-137">RELATED LINKS</span></span>

[<span data-ttu-id="3cacb-138">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3cacb-138">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="3cacb-139">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="3cacb-139">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="3cacb-140">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3cacb-140">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="3cacb-141">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3cacb-141">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)
