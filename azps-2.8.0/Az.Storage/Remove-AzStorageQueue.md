---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
ms.openlocfilehash: 2afb39aafacef354c4e50aad1ce0a4824622c9c8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934018"
---
# <span data-ttu-id="95eb0-101">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="95eb0-101">Remove-AzStorageQueue</span></span>

## <span data-ttu-id="95eb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95eb0-102">SYNOPSIS</span></span>
<span data-ttu-id="95eb0-103">Depolama kuyruğunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="95eb0-103">Removes a storage queue.</span></span>

## <span data-ttu-id="95eb0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="95eb0-104">SYNTAX</span></span>

```
Remove-AzStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95eb0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="95eb0-105">DESCRIPTION</span></span>
<span data-ttu-id="95eb0-106">**Remove-AzStorageQueue** cmdlet 'i bir depolama sırasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="95eb0-106">The **Remove-AzStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="95eb0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="95eb0-107">EXAMPLES</span></span>

### <span data-ttu-id="95eb0-108">Örnek 1: depolama kuyruğunu ada göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="95eb0-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzStorageQueue "ContosoQueue01"
```

<span data-ttu-id="95eb0-109">Bu komut, ContosoQueue01 adlı bir sırayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="95eb0-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="95eb0-110">Örnek 2: birden çok depolama sırasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="95eb0-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzStorageQueue "Contoso*" | Remove-AzStorageQueue
```

<span data-ttu-id="95eb0-111">Bu komut, contoso ile başlayan tüm sıraları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="95eb0-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="95eb0-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="95eb0-112">PARAMETERS</span></span>

### <span data-ttu-id="95eb0-113">-Context</span><span class="sxs-lookup"><span data-stu-id="95eb0-113">-Context</span></span>
<span data-ttu-id="95eb0-114">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="95eb0-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="95eb0-115">Depolama bağlamını edinmek için New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95eb0-115">To obtain the storage context, the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="95eb0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95eb0-116">-DefaultProfile</span></span>
<span data-ttu-id="95eb0-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="95eb0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95eb0-118">-Force</span><span class="sxs-lookup"><span data-stu-id="95eb0-118">-Force</span></span>
<span data-ttu-id="95eb0-119">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="95eb0-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="95eb0-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="95eb0-120">-Name</span></span>
<span data-ttu-id="95eb0-121">Kaldırılacak sıranın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="95eb0-121">Specifies the name of the queue to remove.</span></span>

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

### <span data-ttu-id="95eb0-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="95eb0-122">-PassThru</span></span>
<span data-ttu-id="95eb0-123">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="95eb0-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="95eb0-124">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="95eb0-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="95eb0-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="95eb0-125">-Confirm</span></span>
<span data-ttu-id="95eb0-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="95eb0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95eb0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95eb0-127">-WhatIf</span></span>
<span data-ttu-id="95eb0-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="95eb0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95eb0-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="95eb0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95eb0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95eb0-130">CommonParameters</span></span>
<span data-ttu-id="95eb0-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="95eb0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95eb0-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95eb0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95eb0-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="95eb0-133">INPUTS</span></span>

### <span data-ttu-id="95eb0-134">System. String</span><span class="sxs-lookup"><span data-stu-id="95eb0-134">System.String</span></span>

### <span data-ttu-id="95eb0-135">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="95eb0-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="95eb0-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="95eb0-136">OUTPUTS</span></span>

### <span data-ttu-id="95eb0-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="95eb0-137">System.Boolean</span></span>

## <span data-ttu-id="95eb0-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="95eb0-138">NOTES</span></span>

## <span data-ttu-id="95eb0-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="95eb0-139">RELATED LINKS</span></span>

[<span data-ttu-id="95eb0-140">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="95eb0-140">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="95eb0-141">Yeni-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="95eb0-141">New-AzStorageQueue</span></span>](./New-AzStorageQueue.md)
