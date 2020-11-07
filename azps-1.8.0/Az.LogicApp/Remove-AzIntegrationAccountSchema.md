---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 56550997-21D9-4F85-B23A-677625482547
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountSchema.md
ms.openlocfilehash: 1137ba802bc1ccd920b45c895b70aee2f8a8e7ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915979"
---
# <span data-ttu-id="0da02-101">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="0da02-101">Remove-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="0da02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0da02-102">SYNOPSIS</span></span>
<span data-ttu-id="0da02-103">Tümleştirme hesabı şemasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0da02-103">Removes an integration account schema.</span></span>

## <span data-ttu-id="0da02-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0da02-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0da02-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0da02-105">DESCRIPTION</span></span>
<span data-ttu-id="0da02-106">**Remove-Azıntegrationaccountschema** cmdlet 'i, bir kaynak grubundan tümleştirme hesabı şemasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0da02-106">The **Remove-AzIntegrationAccountSchema** cmdlet removes an integration account schema from a resource group.</span></span>
<span data-ttu-id="0da02-107">Tümleştirme hesap adını, kaynak grubu adını ve şema adını belirtme.</span><span class="sxs-lookup"><span data-stu-id="0da02-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="0da02-108">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="0da02-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="0da02-109">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="0da02-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="0da02-110">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="0da02-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0da02-111">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="0da02-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0da02-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0da02-112">EXAMPLES</span></span>

### <span data-ttu-id="0da02-113">Örnek 1: Tümleştirme hesabı şemasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="0da02-113">Example 1: Remove an integration account schema</span></span>
```
PS C:\>Remove-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
```

<span data-ttu-id="0da02-114">Bu komut, IntegrationAccountSchema43 adlı bir tümleştirme hesabı şemasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0da02-114">This command removes an integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="0da02-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0da02-115">PARAMETERS</span></span>

### <span data-ttu-id="0da02-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0da02-116">-DefaultProfile</span></span>
<span data-ttu-id="0da02-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0da02-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0da02-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0da02-118">-Force</span></span>
<span data-ttu-id="0da02-119">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="0da02-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0da02-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="0da02-120">-Name</span></span>
<span data-ttu-id="0da02-121">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0da02-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="0da02-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0da02-122">-ResourceGroupName</span></span>
<span data-ttu-id="0da02-123">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0da02-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0da02-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="0da02-124">-SchemaName</span></span>
<span data-ttu-id="0da02-125">Tümleştirme hesabı şemasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0da02-125">Specifies the name of an integration account schema.</span></span>

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

### <span data-ttu-id="0da02-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="0da02-126">-Confirm</span></span>
<span data-ttu-id="0da02-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0da02-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0da02-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0da02-128">-WhatIf</span></span>
<span data-ttu-id="0da02-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0da02-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0da02-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0da02-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0da02-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0da02-131">CommonParameters</span></span>
<span data-ttu-id="0da02-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0da02-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0da02-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0da02-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0da02-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0da02-134">INPUTS</span></span>

### <span data-ttu-id="0da02-135">System. String</span><span class="sxs-lookup"><span data-stu-id="0da02-135">System.String</span></span>

## <span data-ttu-id="0da02-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0da02-136">OUTPUTS</span></span>

### <span data-ttu-id="0da02-137">System. void</span><span class="sxs-lookup"><span data-stu-id="0da02-137">System.Void</span></span>

## <span data-ttu-id="0da02-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0da02-138">NOTES</span></span>

## <span data-ttu-id="0da02-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0da02-139">RELATED LINKS</span></span>

[<span data-ttu-id="0da02-140">Get-Azıntegrationaccountschema</span><span class="sxs-lookup"><span data-stu-id="0da02-140">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="0da02-141">Yeni-Azıntegrationaccountschema</span><span class="sxs-lookup"><span data-stu-id="0da02-141">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="0da02-142">Set-Azıntegrationaccountschema</span><span class="sxs-lookup"><span data-stu-id="0da02-142">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


