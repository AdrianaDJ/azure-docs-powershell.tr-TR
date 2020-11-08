---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
ms.openlocfilehash: 2cc10a1b72dc369aef08b84e7b8fe2128ff0ac33
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275803"
---
# <span data-ttu-id="38ac2-101">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="38ac2-101">Remove-AzStorageQueue</span></span>

## <span data-ttu-id="38ac2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38ac2-102">SYNOPSIS</span></span>
<span data-ttu-id="38ac2-103">Depolama kuyruğunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="38ac2-103">Removes a storage queue.</span></span>

## <span data-ttu-id="38ac2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="38ac2-104">SYNTAX</span></span>

```
Remove-AzStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38ac2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="38ac2-105">DESCRIPTION</span></span>
<span data-ttu-id="38ac2-106">**Remove-AzStorageQueue** cmdlet 'i bir depolama sırasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="38ac2-106">The **Remove-AzStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="38ac2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="38ac2-107">EXAMPLES</span></span>

### <span data-ttu-id="38ac2-108">Örnek 1: depolama kuyruğunu ada göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="38ac2-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzStorageQueue "ContosoQueue01"
```

<span data-ttu-id="38ac2-109">Bu komut, ContosoQueue01 adlı bir sırayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="38ac2-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="38ac2-110">Örnek 2: birden çok depolama sırasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="38ac2-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzStorageQueue "Contoso*" | Remove-AzStorageQueue
```

<span data-ttu-id="38ac2-111">Bu komut, contoso ile başlayan tüm sıraları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="38ac2-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="38ac2-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="38ac2-112">PARAMETERS</span></span>

### <span data-ttu-id="38ac2-113">-Context</span><span class="sxs-lookup"><span data-stu-id="38ac2-113">-Context</span></span>
<span data-ttu-id="38ac2-114">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="38ac2-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="38ac2-115">Depolama bağlamını edinmek için New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38ac2-115">To obtain the storage context, the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="38ac2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38ac2-116">-DefaultProfile</span></span>
<span data-ttu-id="38ac2-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="38ac2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38ac2-118">-Force</span><span class="sxs-lookup"><span data-stu-id="38ac2-118">-Force</span></span>
<span data-ttu-id="38ac2-119">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="38ac2-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="38ac2-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="38ac2-120">-Name</span></span>
<span data-ttu-id="38ac2-121">Kaldırılacak sıranın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="38ac2-121">Specifies the name of the queue to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38ac2-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="38ac2-122">-PassThru</span></span>
<span data-ttu-id="38ac2-123">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="38ac2-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="38ac2-124">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="38ac2-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="38ac2-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="38ac2-125">-Confirm</span></span>
<span data-ttu-id="38ac2-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="38ac2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38ac2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38ac2-127">-WhatIf</span></span>
<span data-ttu-id="38ac2-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="38ac2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38ac2-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="38ac2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38ac2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38ac2-130">CommonParameters</span></span>
<span data-ttu-id="38ac2-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="38ac2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38ac2-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38ac2-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38ac2-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="38ac2-133">INPUTS</span></span>

### <span data-ttu-id="38ac2-134">System. String</span><span class="sxs-lookup"><span data-stu-id="38ac2-134">System.String</span></span>

### <span data-ttu-id="38ac2-135">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="38ac2-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="38ac2-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="38ac2-136">OUTPUTS</span></span>

### <span data-ttu-id="38ac2-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="38ac2-137">System.Boolean</span></span>

## <span data-ttu-id="38ac2-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="38ac2-138">NOTES</span></span>

## <span data-ttu-id="38ac2-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="38ac2-139">RELATED LINKS</span></span>

[<span data-ttu-id="38ac2-140">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="38ac2-140">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="38ac2-141">Yeni-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="38ac2-141">New-AzStorageQueue</span></span>](./New-AzStorageQueue.md)
