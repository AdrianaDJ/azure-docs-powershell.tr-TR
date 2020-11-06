---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueue.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 51ea3111b5010b0e29f7bfd69ed5a8e66e596113
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588329"
---
# <span data-ttu-id="c775d-101">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="c775d-101">Remove-AzureStorageQueue</span></span>

## <span data-ttu-id="c775d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c775d-102">SYNOPSIS</span></span>
<span data-ttu-id="c775d-103">Depolama kuyruğunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c775d-103">Removes a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c775d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c775d-104">SYNTAX</span></span>

```
Remove-AzureStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c775d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c775d-105">DESCRIPTION</span></span>
<span data-ttu-id="c775d-106">**Remove-AzureStorageQueue** cmdlet 'i bir depolama sırasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c775d-106">The **Remove-AzureStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="c775d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c775d-107">EXAMPLES</span></span>

### <span data-ttu-id="c775d-108">Örnek 1: depolama kuyruğunu ada göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="c775d-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzureStorageQueue "ContosoQueue01"
```

<span data-ttu-id="c775d-109">Bu komut, ContosoQueue01 adlı bir sırayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c775d-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="c775d-110">Örnek 2: birden çok depolama sırasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="c775d-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue "Contoso*" | Remove-AzureStorageQueue
```

<span data-ttu-id="c775d-111">Bu komut, contoso ile başlayan tüm sıraları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c775d-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="c775d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c775d-112">PARAMETERS</span></span>

### <span data-ttu-id="c775d-113">-Context</span><span class="sxs-lookup"><span data-stu-id="c775d-113">-Context</span></span>
<span data-ttu-id="c775d-114">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c775d-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="c775d-115">Depolama bağlamını edinmek için New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c775d-115">To obtain the storage context, the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c775d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c775d-116">-Force</span></span>
<span data-ttu-id="c775d-117">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="c775d-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c775d-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="c775d-118">-Name</span></span>
<span data-ttu-id="c775d-119">Kaldırılacak sıranın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c775d-119">Specifies the name of the queue to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c775d-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c775d-120">-PassThru</span></span>
<span data-ttu-id="c775d-121">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="c775d-121">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="c775d-122">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="c775d-122">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="c775d-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="c775d-123">-Confirm</span></span>
<span data-ttu-id="c775d-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c775d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c775d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c775d-125">-WhatIf</span></span>
<span data-ttu-id="c775d-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c775d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c775d-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c775d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c775d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c775d-128">CommonParameters</span></span>
<span data-ttu-id="c775d-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c775d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c775d-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c775d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c775d-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c775d-131">INPUTS</span></span>

### <span data-ttu-id="c775d-132">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="c775d-132">IStorageContext</span></span>

<span data-ttu-id="c775d-133">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="c775d-133">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="c775d-134">Dizisi</span><span class="sxs-lookup"><span data-stu-id="c775d-134">String</span></span>

<span data-ttu-id="c775d-135">' Name ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="c775d-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="c775d-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c775d-136">OUTPUTS</span></span>

### <span data-ttu-id="c775d-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c775d-137">System.Boolean</span></span>

## <span data-ttu-id="c775d-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c775d-138">NOTES</span></span>

## <span data-ttu-id="c775d-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c775d-139">RELATED LINKS</span></span>

[<span data-ttu-id="c775d-140">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="c775d-140">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="c775d-141">Yeni-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="c775d-141">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)
