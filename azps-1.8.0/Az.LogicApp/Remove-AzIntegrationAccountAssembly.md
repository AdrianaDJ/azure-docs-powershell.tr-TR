---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
ms.openlocfilehash: ce3a3ae24a1064e036bc66e0fa7bfdaa6c74e0c5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916004"
---
# <span data-ttu-id="b00c8-101">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b00c8-101">Remove-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="b00c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b00c8-102">SYNOPSIS</span></span>
<span data-ttu-id="b00c8-103">Tümleştirme hesabı derlemesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b00c8-103">Removes an integration account assembly.</span></span>

## <span data-ttu-id="b00c8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b00c8-104">SYNTAX</span></span>

### <span data-ttu-id="b00c8-105">Byıntegrationaccount (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b00c8-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b00c8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b00c8-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b00c8-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="b00c8-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b00c8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b00c8-108">DESCRIPTION</span></span>
<span data-ttu-id="b00c8-109">**Remove-AzIntegrationAccountAssembly** cmdlet 'i, tümleştirme hesabından derleme kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b00c8-109">The **Remove-AzIntegrationAccountAssembly** cmdlet removes an assembly from an integration account.</span></span>

## <span data-ttu-id="b00c8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b00c8-110">EXAMPLES</span></span>

### <span data-ttu-id="b00c8-111">Örnek 1: bir derlemeyi parametrelerle kaldırma</span><span class="sxs-lookup"><span data-stu-id="b00c8-111">Example 1: Remove an assembly by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"
```

<span data-ttu-id="b00c8-112">"Sampleıntegrationaccount" tümleştirme hesabında bulunan "sampleAssembly" adlı derlemeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b00c8-112">Removes the assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="b00c8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b00c8-113">PARAMETERS</span></span>

### <span data-ttu-id="b00c8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b00c8-114">-DefaultProfile</span></span>
<span data-ttu-id="b00c8-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b00c8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b00c8-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b00c8-116">-InputObject</span></span>
<span data-ttu-id="b00c8-117">Tümleştirme hesabı derlemesi.</span><span class="sxs-lookup"><span data-stu-id="b00c8-117">An integration account assembly.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b00c8-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="b00c8-118">-Name</span></span>
<span data-ttu-id="b00c8-119">Tümleştirme hesabı derleme adı.</span><span class="sxs-lookup"><span data-stu-id="b00c8-119">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: AssemblyName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b00c8-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="b00c8-120">-ParentName</span></span>
<span data-ttu-id="b00c8-121">Tümleştirme hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="b00c8-121">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b00c8-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b00c8-122">-PassThru</span></span>
<span data-ttu-id="b00c8-123">Komutun başarılı olup olmadığını döndürün.</span><span class="sxs-lookup"><span data-stu-id="b00c8-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="b00c8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b00c8-124">-ResourceGroupName</span></span>
<span data-ttu-id="b00c8-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b00c8-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b00c8-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b00c8-126">-ResourceId</span></span>
<span data-ttu-id="b00c8-127">Tümleştirme hesabı derleme kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="b00c8-127">The integration account assembly resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b00c8-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="b00c8-128">-Confirm</span></span>
<span data-ttu-id="b00c8-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b00c8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b00c8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b00c8-130">-WhatIf</span></span>
<span data-ttu-id="b00c8-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b00c8-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b00c8-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b00c8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b00c8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b00c8-133">CommonParameters</span></span>
<span data-ttu-id="b00c8-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b00c8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b00c8-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b00c8-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b00c8-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b00c8-136">INPUTS</span></span>

### <span data-ttu-id="b00c8-137">Microsoft. Azure. Commands. Logicuyg. modeller. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="b00c8-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="b00c8-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b00c8-138">System.String</span></span>

## <span data-ttu-id="b00c8-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b00c8-139">OUTPUTS</span></span>

### <span data-ttu-id="b00c8-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b00c8-140">System.Boolean</span></span>

## <span data-ttu-id="b00c8-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b00c8-141">NOTES</span></span>

## <span data-ttu-id="b00c8-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b00c8-142">RELATED LINKS</span></span>