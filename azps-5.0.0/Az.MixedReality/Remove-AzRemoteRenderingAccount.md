---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/remove-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzRemoteRenderingAccount.md
ms.openlocfilehash: bfcbaa723dc2d06d74ba4d515affd2f19a51ec3e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277300"
---
# <span data-ttu-id="e020a-101">Remove-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="e020a-101">Remove-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="e020a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e020a-102">SYNOPSIS</span></span>
<span data-ttu-id="e020a-103">Uzaktan Işleme hesabını silme</span><span class="sxs-lookup"><span data-stu-id="e020a-103">Delete Remote Rendering Account</span></span>

## <span data-ttu-id="e020a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e020a-104">SYNTAX</span></span>

### <span data-ttu-id="e020a-105">DefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e020a-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e020a-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="e020a-106">ResourceIdParameterSet</span></span>
```
Remove-AzRemoteRenderingAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e020a-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="e020a-107">PipelineParameterSet</span></span>
```
Remove-AzRemoteRenderingAccount -InputObject <PSRemoteRenderingAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e020a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e020a-108">DESCRIPTION</span></span>
<span data-ttu-id="e020a-109">Belirtilen uzaktan Işleme hesabını belirli bir abonelikten ve kaynak grubundan silin.</span><span class="sxs-lookup"><span data-stu-id="e020a-109">Delete specified Remote Rendering Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="e020a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e020a-110">EXAMPLES</span></span>

### <span data-ttu-id="e020a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e020a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="e020a-112">"Örnek" uzaktan Işleme hesabını geçerli abonelikten ve "RG1" kaynak grubundan silme.</span><span class="sxs-lookup"><span data-stu-id="e020a-112">Delete Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="e020a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e020a-113">PARAMETERS</span></span>

### <span data-ttu-id="e020a-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="e020a-114">-Confirm</span></span>
<span data-ttu-id="e020a-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e020a-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e020a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e020a-116">-DefaultProfile</span></span>
<span data-ttu-id="e020a-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e020a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e020a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e020a-118">-InputObject</span></span>
<span data-ttu-id="e020a-119">Özel etki alanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e020a-119">The custom domain object.</span></span>

```yaml
Type: PSRemoteRenderingAccount
Parameter Sets: PipelineParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e020a-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="e020a-120">-Name</span></span>
<span data-ttu-id="e020a-121">Uzaktan Işleme hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="e020a-121">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e020a-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e020a-122">-PassThru</span></span>
<span data-ttu-id="e020a-123">Belirtilmişse nesneyi döndür.</span><span class="sxs-lookup"><span data-stu-id="e020a-123">Return object if specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e020a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e020a-124">-ResourceGroupName</span></span>
<span data-ttu-id="e020a-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e020a-125">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e020a-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e020a-126">-ResourceId</span></span>
<span data-ttu-id="e020a-127">Uzaktan Işleme hesabı kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e020a-127">Resource ID of Remote Rendering Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e020a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e020a-128">-WhatIf</span></span>
<span data-ttu-id="e020a-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e020a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e020a-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e020a-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e020a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e020a-131">CommonParameters</span></span>
<span data-ttu-id="e020a-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e020a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e020a-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e020a-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e020a-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e020a-134">INPUTS</span></span>

### <span data-ttu-id="e020a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e020a-135">System.String</span></span>

### <span data-ttu-id="e020a-136">Microsoft. Azure. Commands. MixedReality. RemoteRenderingAccount. PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="e020a-136">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

### <span data-ttu-id="e020a-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e020a-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e020a-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e020a-138">OUTPUTS</span></span>

### <span data-ttu-id="e020a-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e020a-139">System.Boolean</span></span>

## <span data-ttu-id="e020a-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e020a-140">NOTES</span></span>

## <span data-ttu-id="e020a-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e020a-141">RELATED LINKS</span></span>
