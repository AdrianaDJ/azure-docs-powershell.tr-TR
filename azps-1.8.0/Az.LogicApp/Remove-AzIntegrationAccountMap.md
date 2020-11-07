---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7AAF2ACC-84ED-449C-B1E8-F074463F44EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountMap.md
ms.openlocfilehash: 7342601bba3c963131728f02773cb3b84e917bb9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915999"
---
# <span data-ttu-id="4e707-101">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="4e707-101">Remove-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="4e707-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e707-102">SYNOPSIS</span></span>
<span data-ttu-id="4e707-103">Tümleştirme hesabı haritasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4e707-103">Removes an integration account map.</span></span>

## <span data-ttu-id="4e707-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4e707-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e707-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4e707-105">DESCRIPTION</span></span>
<span data-ttu-id="4e707-106">**Remove-Azıntegrationaccountmap** cmdlet 'i, bir kaynak grubundan tümleştirme hesabı haritasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4e707-106">The **Remove-AzIntegrationAccountMap** cmdlet removes an integration account map from a resource group.</span></span>
<span data-ttu-id="4e707-107">Tümleştirme hesap adını, kaynak grubu adını ve harita adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="4e707-107">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="4e707-108">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="4e707-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="4e707-109">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="4e707-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="4e707-110">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="4e707-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4e707-111">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="4e707-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="4e707-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4e707-112">EXAMPLES</span></span>

### <span data-ttu-id="4e707-113">Örnek 1: Tümleştirme hesabı haritasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="4e707-113">Example 1: Remove an integration account map</span></span>
```
PS C:\>Remove-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
```

<span data-ttu-id="4e707-114">Bu komut, IntegrationAccountMap47 adlı tümleştirme hesabı haritasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4e707-114">This command removes the integration account map named IntegrationAccountMap47.</span></span>

## <span data-ttu-id="4e707-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4e707-115">PARAMETERS</span></span>

### <span data-ttu-id="4e707-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e707-116">-DefaultProfile</span></span>
<span data-ttu-id="4e707-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4e707-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e707-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4e707-118">-Force</span></span>
<span data-ttu-id="4e707-119">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="4e707-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4e707-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="4e707-120">-MapName</span></span>
<span data-ttu-id="4e707-121">Tümleştirme hesabı eşlemesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e707-121">Specifies the name of the integration account map.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e707-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="4e707-122">-Name</span></span>
<span data-ttu-id="4e707-123">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e707-123">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e707-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e707-124">-ResourceGroupName</span></span>
<span data-ttu-id="4e707-125">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4e707-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e707-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="4e707-126">-Confirm</span></span>
<span data-ttu-id="4e707-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4e707-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e707-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e707-128">-WhatIf</span></span>
<span data-ttu-id="4e707-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4e707-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e707-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4e707-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e707-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e707-131">CommonParameters</span></span>
<span data-ttu-id="4e707-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4e707-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e707-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e707-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e707-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4e707-134">INPUTS</span></span>

### <span data-ttu-id="4e707-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4e707-135">System.String</span></span>

## <span data-ttu-id="4e707-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4e707-136">OUTPUTS</span></span>

### <span data-ttu-id="4e707-137">System. void</span><span class="sxs-lookup"><span data-stu-id="4e707-137">System.Void</span></span>

## <span data-ttu-id="4e707-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4e707-138">NOTES</span></span>

## <span data-ttu-id="4e707-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4e707-139">RELATED LINKS</span></span>

[<span data-ttu-id="4e707-140">Get-Azıntegrationaccountmap</span><span class="sxs-lookup"><span data-stu-id="4e707-140">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="4e707-141">Yeni-Azıntegrationaccountmap</span><span class="sxs-lookup"><span data-stu-id="4e707-141">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="4e707-142">Set-Azıntegrationaccountmap</span><span class="sxs-lookup"><span data-stu-id="4e707-142">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


