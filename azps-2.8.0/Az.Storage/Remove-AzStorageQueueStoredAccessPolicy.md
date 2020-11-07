---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 32bf76e80dbd088b133d4401dc51bb1f49b2593b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934016"
---
# <span data-ttu-id="d0e9a-101">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d0e9a-101">Remove-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="d0e9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0e9a-102">SYNOPSIS</span></span>
<span data-ttu-id="d0e9a-103">Depolanan bir Access ilkesini Azure depolama sırasından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d0e9a-103">Removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="d0e9a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d0e9a-104">SYNTAX</span></span>

```
Remove-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d0e9a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d0e9a-105">DESCRIPTION</span></span>
<span data-ttu-id="d0e9a-106">**Remove-AzStorageQueueStoredAccessPolicy** cmdlet 'i Azure depolama sırasından depolanan bir Access ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d0e9a-106">The **Remove-AzStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="d0e9a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d0e9a-107">EXAMPLES</span></span>

### <span data-ttu-id="d0e9a-108">Örnek 1: depolanan bir erişim ilkesini depolama sırasından kaldırma</span><span class="sxs-lookup"><span data-stu-id="d0e9a-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="d0e9a-109">Bu komut, Policy04 adındaki bir erişim ilkesini MyQueue adındaki depolama sırasından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d0e9a-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="d0e9a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d0e9a-110">PARAMETERS</span></span>

### <span data-ttu-id="d0e9a-111">-Context</span><span class="sxs-lookup"><span data-stu-id="d0e9a-111">-Context</span></span>
<span data-ttu-id="d0e9a-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0e9a-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d0e9a-113">Depolama bağlamı edinmek için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d0e9a-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d0e9a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0e9a-114">-DefaultProfile</span></span>
<span data-ttu-id="d0e9a-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d0e9a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0e9a-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d0e9a-116">-PassThru</span></span>
<span data-ttu-id="d0e9a-117">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="d0e9a-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="d0e9a-118">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="d0e9a-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="d0e9a-119">-İlke</span><span class="sxs-lookup"><span data-stu-id="d0e9a-119">-Policy</span></span>
<span data-ttu-id="d0e9a-120">Bu cmdlet 'in kaldırdığı depolanan erişim ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0e9a-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d0e9a-121">-Sıra</span><span class="sxs-lookup"><span data-stu-id="d0e9a-121">-Queue</span></span>
<span data-ttu-id="d0e9a-122">Azure depolama sırası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0e9a-122">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="d0e9a-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="d0e9a-123">-Confirm</span></span>
<span data-ttu-id="d0e9a-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d0e9a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0e9a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0e9a-125">-WhatIf</span></span>
<span data-ttu-id="d0e9a-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d0e9a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0e9a-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d0e9a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0e9a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0e9a-128">CommonParameters</span></span>
<span data-ttu-id="d0e9a-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d0e9a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0e9a-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0e9a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0e9a-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d0e9a-131">INPUTS</span></span>

### <span data-ttu-id="d0e9a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d0e9a-132">System.String</span></span>

### <span data-ttu-id="d0e9a-133">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="d0e9a-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d0e9a-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d0e9a-134">OUTPUTS</span></span>

### <span data-ttu-id="d0e9a-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d0e9a-135">System.Boolean</span></span>

## <span data-ttu-id="d0e9a-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d0e9a-136">NOTES</span></span>

## <span data-ttu-id="d0e9a-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d0e9a-137">RELATED LINKS</span></span>

[<span data-ttu-id="d0e9a-138">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d0e9a-138">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="d0e9a-139">Yeni-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d0e9a-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="d0e9a-140">Yeni-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d0e9a-140">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="d0e9a-141">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d0e9a-141">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)
