---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: EBDBB9F0-CA2E-4E4F-9034-3D0FAB88E442
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAgreement.md
ms.openlocfilehash: d320d29a9c5e6136caafde2b7d355a6a2ebf9ca6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751514"
---
# <span data-ttu-id="b3c08-101">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="b3c08-101">Remove-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="b3c08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3c08-102">SYNOPSIS</span></span>
<span data-ttu-id="b3c08-103">Tümleştirme hesabı anlaşmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b3c08-103">Removes an integration account agreement.</span></span>

## <span data-ttu-id="b3c08-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b3c08-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3c08-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b3c08-105">DESCRIPTION</span></span>
<span data-ttu-id="b3c08-106">**Remove-Azıntegrationaccountagreement** cmdlet 'ı bir Azure kaynak grubundan tümleştirme hesabı anlaşmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b3c08-106">The **Remove-AzIntegrationAccountAgreement** cmdlet removes an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="b3c08-107">Tümleştirme hesap adını, kaynak grubu adını ve anlaşma adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="b3c08-107">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="b3c08-108">Bu modül dinamik parametreleri destekler.</span><span class="sxs-lookup"><span data-stu-id="b3c08-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b3c08-109">Dinamik parametre kullanmak için, komuta bunu yazın.</span><span class="sxs-lookup"><span data-stu-id="b3c08-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b3c08-110">Dinamik parametrelerin adlarını keşfetmek için, cmdlet adından sonra bir kısa çizgi (-) yazın ve ardından kullanılabilir parametreler arasında geçiş yapmak için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="b3c08-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b3c08-111">Gerekli bir şablon parametresini atlarsanız, cmdlet bu değeri sorar.</span><span class="sxs-lookup"><span data-stu-id="b3c08-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b3c08-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b3c08-112">EXAMPLES</span></span>

### <span data-ttu-id="b3c08-113">Örnek 1: bir tümleştirme hesabı sözleşmesini ada göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="b3c08-113">Example 1: Remove an integration account agreement by name</span></span>
```
PS C:\>Remove-AzIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06" -Force
```

<span data-ttu-id="b3c08-114">Bu komut, IntegrationAccountAgreement06 adlı tümleştirme hesabı sözleşmesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b3c08-114">This command removes the integration account agreement named IntegrationAccountAgreement06.</span></span>
<span data-ttu-id="b3c08-115">Komut sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="b3c08-115">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="b3c08-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b3c08-116">PARAMETERS</span></span>

### <span data-ttu-id="b3c08-117">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="b3c08-117">-AgreementName</span></span>
<span data-ttu-id="b3c08-118">Tümleştirme hesap anlaşmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3c08-118">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="b3c08-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3c08-119">-DefaultProfile</span></span>
<span data-ttu-id="b3c08-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b3c08-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3c08-121">-Force</span><span class="sxs-lookup"><span data-stu-id="b3c08-121">-Force</span></span>
<span data-ttu-id="b3c08-122">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="b3c08-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b3c08-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="b3c08-123">-Name</span></span>
<span data-ttu-id="b3c08-124">Tümleştirme hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3c08-124">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="b3c08-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3c08-125">-ResourceGroupName</span></span>
<span data-ttu-id="b3c08-126">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3c08-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b3c08-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="b3c08-127">-Confirm</span></span>
<span data-ttu-id="b3c08-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b3c08-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3c08-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3c08-129">-WhatIf</span></span>
<span data-ttu-id="b3c08-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b3c08-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3c08-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b3c08-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3c08-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3c08-132">CommonParameters</span></span>
<span data-ttu-id="b3c08-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b3c08-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3c08-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3c08-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3c08-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b3c08-135">INPUTS</span></span>

### <span data-ttu-id="b3c08-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b3c08-136">System.String</span></span>

## <span data-ttu-id="b3c08-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b3c08-137">OUTPUTS</span></span>

### <span data-ttu-id="b3c08-138">System. void</span><span class="sxs-lookup"><span data-stu-id="b3c08-138">System.Void</span></span>

## <span data-ttu-id="b3c08-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b3c08-139">NOTES</span></span>

## <span data-ttu-id="b3c08-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b3c08-140">RELATED LINKS</span></span>

[<span data-ttu-id="b3c08-141">Get-Azıntegrationmuhasebe</span><span class="sxs-lookup"><span data-stu-id="b3c08-141">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="b3c08-142">Yeni-azya dili muhasebe</span><span class="sxs-lookup"><span data-stu-id="b3c08-142">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="b3c08-143">Set-Azıntegrationmuhasebe</span><span class="sxs-lookup"><span data-stu-id="b3c08-143">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


