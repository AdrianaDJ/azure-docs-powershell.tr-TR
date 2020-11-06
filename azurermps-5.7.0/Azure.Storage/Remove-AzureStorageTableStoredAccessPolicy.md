---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTableStoredAccessPolicy.md
ms.openlocfilehash: a9e1290c5933d54481c57b051e170568653eee5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592150"
---
# <span data-ttu-id="952c7-101">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="952c7-101">Remove-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="952c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="952c7-102">SYNOPSIS</span></span>
<span data-ttu-id="952c7-103">Depolanan bir Access ilkesini Azure depolama tablosundan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="952c7-103">Removes a stored access policy from an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="952c7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="952c7-104">SYNTAX</span></span>

```
Remove-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="952c7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="952c7-105">DESCRIPTION</span></span>
<span data-ttu-id="952c7-106">**Remove-AzureStorageTableStoredAccessPolicy** cmdlet 'i Azure depolama tablosundan depolanan bir Access ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="952c7-106">The **Remove-AzureStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="952c7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="952c7-107">EXAMPLES</span></span>

### <span data-ttu-id="952c7-108">Örnek 1: depolama tablosundan depolanan bir Access ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="952c7-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="952c7-109">Bu komut, Policy05 adlı depolama tablosundan MyTable adlı ilkeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="952c7-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="952c7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="952c7-110">PARAMETERS</span></span>

### <span data-ttu-id="952c7-111">-Context</span><span class="sxs-lookup"><span data-stu-id="952c7-111">-Context</span></span>
<span data-ttu-id="952c7-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="952c7-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="952c7-113">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="952c7-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="952c7-114">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="952c7-114">-PassThru</span></span>
<span data-ttu-id="952c7-115">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="952c7-115">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="952c7-116">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="952c7-116">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="952c7-117">-İlke</span><span class="sxs-lookup"><span data-stu-id="952c7-117">-Policy</span></span>
<span data-ttu-id="952c7-118">Bu cmdlet 'in kaldırdığı depolanan erişim ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="952c7-118">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="952c7-119">-Tablo</span><span class="sxs-lookup"><span data-stu-id="952c7-119">-Table</span></span>
<span data-ttu-id="952c7-120">Azure tablo adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="952c7-120">Specifies the Azure table name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="952c7-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="952c7-121">-Confirm</span></span>
<span data-ttu-id="952c7-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="952c7-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="952c7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="952c7-123">-WhatIf</span></span>
<span data-ttu-id="952c7-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="952c7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="952c7-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="952c7-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="952c7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="952c7-126">CommonParameters</span></span>
<span data-ttu-id="952c7-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="952c7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="952c7-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="952c7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="952c7-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="952c7-129">INPUTS</span></span>

### <span data-ttu-id="952c7-130">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="952c7-130">IStorageContext</span></span>

<span data-ttu-id="952c7-131">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="952c7-131">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="952c7-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="952c7-132">OUTPUTS</span></span>

### <span data-ttu-id="952c7-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="952c7-133">System.Boolean</span></span>

## <span data-ttu-id="952c7-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="952c7-134">NOTES</span></span>

## <span data-ttu-id="952c7-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="952c7-135">RELATED LINKS</span></span>

[<span data-ttu-id="952c7-136">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="952c7-136">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="952c7-137">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="952c7-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="952c7-138">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="952c7-138">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="952c7-139">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="952c7-139">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)
