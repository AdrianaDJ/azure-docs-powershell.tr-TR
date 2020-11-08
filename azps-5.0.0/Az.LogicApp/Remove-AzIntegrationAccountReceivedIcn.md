---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 2a80173900c0faf062c3d4ba0c0a3b2029737bcf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278958"
---
# <span data-ttu-id="9c9b0-101">Remove-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="9c9b0-101">Remove-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="9c9b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c9b0-102">SYNOPSIS</span></span>
<span data-ttu-id="9c9b0-103">Bu cmdlet, anlaşma ve denetim numarası değeri başına alınan belirli bir değiş tokuş denetim numarasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-103">This cmdlet removes a specific received interchange control number per agreement and control number value.</span></span>

## <span data-ttu-id="9c9b0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9c9b0-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c9b0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9c9b0-105">DESCRIPTION</span></span>
<span data-ttu-id="9c9b0-106">Bu cmdlet, tümleştirme hesabından alınan bir takas kontrol numarasını kaldırmak ve yinelenen numara algılama etkinleştirildiğinde B2B bağlayıcısının iletiyi işlemesi için olağanüstü durum kurtarma senaryolarında kullanılmak üzere tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-106">This cmdlet is meant to be used in disaster recovery scenarios to remove a received interchange control number from the integration account so that the B2B connector may process again the message when duplicate number detection is enabled.</span></span>
<span data-ttu-id="9c9b0-107">Nadir olarak, alınan değişim denetim numarası olağanüstü bir şekilde bir olağanüstü durumda ve B2B Bağlayıcısı alışverişi hatalı olarak reddetmeden önce rezerve edilebilir.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-107">In rare occasions the received interchange control number may be reserved shortly before a disaster and before the B2B connector rejects the interchange as erroneous.</span></span>
<span data-ttu-id="9c9b0-108">Bu gibi durumlarda işlem, yük düzeltildikten sonra kurtarma sitesinin aynı alışverişi yeniden işlemesini etkinleştirmek isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-108">In such occasions the operation may want to enable the recovery site to process again the same interchange after its payload is corrected.</span></span>
<span data-ttu-id="9c9b0-109">Lütfen x12 veya Ediolgu denetim numaralarının döndürülmesini isteyip istemediğinizi belirtmek için "-AgreementType" parametresini sağlayın</span><span class="sxs-lookup"><span data-stu-id="9c9b0-109">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="9c9b0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9c9b0-110">EXAMPLES</span></span>

### <span data-ttu-id="9c9b0-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9c9b0-111">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The existing received control number '000000641' for agreement 'X12AgreementName' is not in a valid format.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], PSInvalidOperationException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand

PS C:\> Remove-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The session 'X12-ICN-X12AgreementName-000000641' could not be found in integration account 'accountName'.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], CloudException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand
```

<span data-ttu-id="9c9b0-112">Alınan bir x12 Interchange Control numarası alma girişimleri geçerli biçimde değil.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-112">Attempts to get a received X12 interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="9c9b0-113">Alınan x12 Interchange Control numarasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-113">Removes the received X12 interchange control number.</span></span>
<span data-ttu-id="9c9b0-114">Alınan x12 Interchange Control numarasının kaldırıldığını onaylar ve yeniden alınmaya çalışılmamıştır.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-114">Confirms the received X12 interchange control number was removed by attempting to get it again.</span></span>

### <span data-ttu-id="9c9b0-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="9c9b0-115">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The existing received control number '000000641' for agreement 'EdifactAgreementName' is not in a valid format.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], PSInvalidOperationException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand

PS C:\> Remove-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The session 'Edifact-ICN-EdifactAgreementName-000000641' could not be found in integration account 'accountName'.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], CloudException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand
```

<span data-ttu-id="9c9b0-116">Alınan bir Ediolgu değişim denetimi numarası alma girişimleri, hangi içeriğin geçerli bir biçimde olmadığı.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-116">Attempts to get a received Edifact interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="9c9b0-117">Alınan Ediolgu değişim denetim numarasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-117">Removes the received Edifact interchange control number.</span></span>
<span data-ttu-id="9c9b0-118">Alınan Ediolgu değişim denetim numarasının kaldırıldığını onaylar ve yeniden alınmaya çalışılmaya çalışıyor.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-118">Confirms the received Edifact interchange control number was removed by attempting to get it again.</span></span>

## <span data-ttu-id="9c9b0-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9c9b0-119">PARAMETERS</span></span>

### <span data-ttu-id="9c9b0-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="9c9b0-120">-AgreementName</span></span>
<span data-ttu-id="9c9b0-121">Tümleştirme hesabı anlaşma adı.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="9c9b0-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="9c9b0-122">-AgreementType</span></span>
<span data-ttu-id="9c9b0-123">Tümleştirme hesabı anlaşma türü.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-123">The integration account agreement type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MessageType
Accepted values: X12, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c9b0-124">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="9c9b0-124">-ControlNumberValue</span></span>
<span data-ttu-id="9c9b0-125">Tümleştirme hesabı kontrol numarası değeri.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-125">The integration account control number value.</span></span>

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

### <span data-ttu-id="9c9b0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c9b0-126">-DefaultProfile</span></span>
<span data-ttu-id="9c9b0-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9c9b0-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9c9b0-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="9c9b0-128">-Name</span></span>
<span data-ttu-id="9c9b0-129">Tümleştirme hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-129">The integration account name.</span></span>

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

### <span data-ttu-id="9c9b0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c9b0-130">-ResourceGroupName</span></span>
<span data-ttu-id="9c9b0-131">Tümleştirme hesabı kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="9c9b0-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="9c9b0-132">-Confirm</span></span>
<span data-ttu-id="9c9b0-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c9b0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c9b0-134">-WhatIf</span></span>
<span data-ttu-id="9c9b0-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c9b0-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c9b0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c9b0-137">CommonParameters</span></span>
<span data-ttu-id="9c9b0-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9c9b0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c9b0-139">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c9b0-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c9b0-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9c9b0-140">INPUTS</span></span>

### <span data-ttu-id="9c9b0-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9c9b0-141">System.String</span></span>

## <span data-ttu-id="9c9b0-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9c9b0-142">OUTPUTS</span></span>

### <span data-ttu-id="9c9b0-143">System. void</span><span class="sxs-lookup"><span data-stu-id="9c9b0-143">System.Void</span></span>

## <span data-ttu-id="9c9b0-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9c9b0-144">NOTES</span></span>

## <span data-ttu-id="9c9b0-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9c9b0-145">RELATED LINKS</span></span>

<span data-ttu-id="9c9b0-146">[Get-az](./Get-AzIntegrationAccountReceivedIcn.md) 
 [Set-az](./Set-AzIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="9c9b0-146">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md)
[Set-AzIntegrationAccountReceivedIcn](./Set-AzIntegrationAccountReceivedIcn.md)</span></span>

