---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: f5620baf0cbd2f5c195b981787ac9def98851fe2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937502"
---
# <span data-ttu-id="19472-101">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="19472-101">Remove-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="19472-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19472-102">SYNOPSIS</span></span>
<span data-ttu-id="19472-103">Depolanan bir Access ilkesini Azure depolama sırasından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="19472-103">Removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="19472-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="19472-104">SYNTAX</span></span>

```
Remove-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="19472-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="19472-105">DESCRIPTION</span></span>
<span data-ttu-id="19472-106">**Remove-AzStorageQueueStoredAccessPolicy** cmdlet 'i Azure depolama sırasından depolanan bir Access ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="19472-106">The **Remove-AzStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="19472-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="19472-107">EXAMPLES</span></span>

### <span data-ttu-id="19472-108">Örnek 1: depolanan bir erişim ilkesini depolama sırasından kaldırma</span><span class="sxs-lookup"><span data-stu-id="19472-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="19472-109">Bu komut, Policy04 adındaki bir erişim ilkesini MyQueue adındaki depolama sırasından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="19472-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="19472-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="19472-110">PARAMETERS</span></span>

### <span data-ttu-id="19472-111">-Context</span><span class="sxs-lookup"><span data-stu-id="19472-111">-Context</span></span>
<span data-ttu-id="19472-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="19472-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="19472-113">Depolama bağlamı edinmek için New-AzStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="19472-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="19472-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19472-114">-DefaultProfile</span></span>
<span data-ttu-id="19472-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="19472-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19472-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="19472-116">-PassThru</span></span>
<span data-ttu-id="19472-117">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="19472-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="19472-118">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="19472-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="19472-119">-İlke</span><span class="sxs-lookup"><span data-stu-id="19472-119">-Policy</span></span>
<span data-ttu-id="19472-120">Bu cmdlet 'in kaldırdığı depolanan erişim ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="19472-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="19472-121">-Sıra</span><span class="sxs-lookup"><span data-stu-id="19472-121">-Queue</span></span>
<span data-ttu-id="19472-122">Azure depolama sırası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="19472-122">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="19472-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="19472-123">-Confirm</span></span>
<span data-ttu-id="19472-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="19472-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19472-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19472-125">-WhatIf</span></span>
<span data-ttu-id="19472-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="19472-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19472-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="19472-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19472-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19472-128">CommonParameters</span></span>
<span data-ttu-id="19472-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="19472-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19472-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19472-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19472-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="19472-131">INPUTS</span></span>

### <span data-ttu-id="19472-132">System. String</span><span class="sxs-lookup"><span data-stu-id="19472-132">System.String</span></span>

### <span data-ttu-id="19472-133">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="19472-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="19472-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="19472-134">OUTPUTS</span></span>

### <span data-ttu-id="19472-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="19472-135">System.Boolean</span></span>

## <span data-ttu-id="19472-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="19472-136">NOTES</span></span>

## <span data-ttu-id="19472-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="19472-137">RELATED LINKS</span></span>

[<span data-ttu-id="19472-138">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="19472-138">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="19472-139">Yeni-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="19472-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="19472-140">Yeni-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="19472-140">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="19472-141">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="19472-141">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)
