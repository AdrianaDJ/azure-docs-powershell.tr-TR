---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 56550997-21D9-4F85-B23A-677625482547
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountSchema.md
ms.openlocfilehash: 50eab845d20d9bf95c20e94f6309be2a302f413c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104337"
---
# <span data-ttu-id="8b58e-101">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="8b58e-101">Remove-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="8b58e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b58e-102">SYNOPSIS</span></span>
<span data-ttu-id="8b58e-103">Tümleştirme hesabı şemasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8b58e-103">Removes an integration account schema.</span></span>

## <span data-ttu-id="8b58e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8b58e-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b58e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8b58e-105">DESCRIPTION</span></span>
<span data-ttu-id="8b58e-106">**Remove-Azıntegrationaccountschema** cmdlet 'i, bir kaynak grubundan tümleştirme hesabı şemasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8b58e-106">The **Remove-AzIntegrationAccountSchema** cmdlet removes an integration account schema from a resource group.</span></span>
<span data-ttu-id="8b58e-107">Tümleştirme hesap adını, kaynak grubu adını ve şema adını belirtme.</span><span class="sxs-lookup"><span data-stu-id="8b58e-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="8b58e-108">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="8b58e-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="8b58e-109">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="8b58e-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="8b58e-110">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="8b58e-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8b58e-111">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="8b58e-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="8b58e-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8b58e-112">EXAMPLES</span></span>

### <span data-ttu-id="8b58e-113">Örnek 1: Tümleştirme hesabı şemasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="8b58e-113">Example 1: Remove an integration account schema</span></span>
```
PS C:\>Remove-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
```

<span data-ttu-id="8b58e-114">Bu komut, IntegrationAccountSchema43 adlı bir tümleştirme hesabı şemasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8b58e-114">This command removes an integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="8b58e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8b58e-115">PARAMETERS</span></span>

### <span data-ttu-id="8b58e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b58e-116">-DefaultProfile</span></span>
<span data-ttu-id="8b58e-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8b58e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b58e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="8b58e-118">-Force</span></span>
<span data-ttu-id="8b58e-119">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="8b58e-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8b58e-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="8b58e-120">-Name</span></span>
<span data-ttu-id="8b58e-121">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b58e-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="8b58e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b58e-122">-ResourceGroupName</span></span>
<span data-ttu-id="8b58e-123">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b58e-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8b58e-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="8b58e-124">-SchemaName</span></span>
<span data-ttu-id="8b58e-125">Tümleştirme hesabı şemasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8b58e-125">Specifies the name of an integration account schema.</span></span>

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

### <span data-ttu-id="8b58e-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="8b58e-126">-Confirm</span></span>
<span data-ttu-id="8b58e-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8b58e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b58e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b58e-128">-WhatIf</span></span>
<span data-ttu-id="8b58e-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8b58e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b58e-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8b58e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b58e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b58e-131">CommonParameters</span></span>
<span data-ttu-id="8b58e-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8b58e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b58e-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b58e-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b58e-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8b58e-134">INPUTS</span></span>

### <span data-ttu-id="8b58e-135">System. String</span><span class="sxs-lookup"><span data-stu-id="8b58e-135">System.String</span></span>

## <span data-ttu-id="8b58e-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8b58e-136">OUTPUTS</span></span>

### <span data-ttu-id="8b58e-137">System. void</span><span class="sxs-lookup"><span data-stu-id="8b58e-137">System.Void</span></span>

## <span data-ttu-id="8b58e-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8b58e-138">NOTES</span></span>

## <span data-ttu-id="8b58e-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8b58e-139">RELATED LINKS</span></span>

[<span data-ttu-id="8b58e-140">Get-Azıntegrationaccountschema</span><span class="sxs-lookup"><span data-stu-id="8b58e-140">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="8b58e-141">Yeni-Azıntegrationaccountschema</span><span class="sxs-lookup"><span data-stu-id="8b58e-141">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="8b58e-142">Set-Azıntegrationaccountschema</span><span class="sxs-lookup"><span data-stu-id="8b58e-142">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


