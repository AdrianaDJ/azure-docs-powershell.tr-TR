---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: E8A557EA-FE3F-4433-BFDE-B4D73DF8467C
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
ms.openlocfilehash: d630a88134b2910a38b21ff964db9748db5cbeeb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915996"
---
# <span data-ttu-id="3418b-101">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="3418b-101">Remove-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="3418b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3418b-102">SYNOPSIS</span></span>
<span data-ttu-id="3418b-103">Tümleştirme hesabı ortağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3418b-103">Removes an integration account partner.</span></span>

## <span data-ttu-id="3418b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3418b-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3418b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3418b-105">DESCRIPTION</span></span>
<span data-ttu-id="3418b-106">**Remove-Azıntegrationaccountpartner** cmdlet 'i, bir kaynak grubundan tümleştirme hesabı ortağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3418b-106">The **Remove-AzIntegrationAccountPartner** cmdlet removes an integration account partner from a resource group.</span></span>
<span data-ttu-id="3418b-107">Tümleştirme hesap adını, kaynak grubu adını ve ortak adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="3418b-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="3418b-108">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="3418b-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3418b-109">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="3418b-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3418b-110">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="3418b-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3418b-111">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="3418b-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3418b-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3418b-112">EXAMPLES</span></span>

### <span data-ttu-id="3418b-113">Örnek 1: Tümleştirme hesabı ortağını kaldırma</span><span class="sxs-lookup"><span data-stu-id="3418b-113">Example 1: Remove an integration account partner</span></span>
```
PS C:\>Remove-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner1"
```

<span data-ttu-id="3418b-114">Bu komut, IntegrationAccountPartner1 adlı tümleştirme hesabı ortağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3418b-114">This command removes the integration account partner named IntegrationAccountPartner1.</span></span>

## <span data-ttu-id="3418b-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3418b-115">PARAMETERS</span></span>

### <span data-ttu-id="3418b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3418b-116">-DefaultProfile</span></span>
<span data-ttu-id="3418b-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3418b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3418b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="3418b-118">-Force</span></span>
<span data-ttu-id="3418b-119">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="3418b-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3418b-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="3418b-120">-Name</span></span>
<span data-ttu-id="3418b-121">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3418b-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="3418b-122">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="3418b-122">-PartnerName</span></span>
<span data-ttu-id="3418b-123">Tümleştirme hesap ortağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3418b-123">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="3418b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3418b-124">-ResourceGroupName</span></span>
<span data-ttu-id="3418b-125">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3418b-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3418b-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="3418b-126">-Confirm</span></span>
<span data-ttu-id="3418b-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3418b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3418b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3418b-128">-WhatIf</span></span>
<span data-ttu-id="3418b-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3418b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3418b-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3418b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3418b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3418b-131">CommonParameters</span></span>
<span data-ttu-id="3418b-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3418b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3418b-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3418b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3418b-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3418b-134">INPUTS</span></span>

### <span data-ttu-id="3418b-135">System. String</span><span class="sxs-lookup"><span data-stu-id="3418b-135">System.String</span></span>

## <span data-ttu-id="3418b-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3418b-136">OUTPUTS</span></span>

### <span data-ttu-id="3418b-137">System. void</span><span class="sxs-lookup"><span data-stu-id="3418b-137">System.Void</span></span>

## <span data-ttu-id="3418b-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3418b-138">NOTES</span></span>

## <span data-ttu-id="3418b-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3418b-139">RELATED LINKS</span></span>

[<span data-ttu-id="3418b-140">Get-Azıntegrationaccountpartner</span><span class="sxs-lookup"><span data-stu-id="3418b-140">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="3418b-141">Yeni-az</span><span class="sxs-lookup"><span data-stu-id="3418b-141">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="3418b-142">Set-Azıntegrationaccountpartner</span><span class="sxs-lookup"><span data-stu-id="3418b-142">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)

