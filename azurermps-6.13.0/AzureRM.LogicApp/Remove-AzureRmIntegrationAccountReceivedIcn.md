---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 429c2eefb9c5ba69b829e292522d168939170e06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590901"
---
# <span data-ttu-id="1b0d4-101">Remove-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="1b0d4-101">Remove-AzureRmIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="1b0d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b0d4-102">SYNOPSIS</span></span>
<span data-ttu-id="1b0d4-103">Bu cmdlet, anlaşma ve denetim numarası değeri başına alınan belirli bir değiş tokuş denetim numarasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1b0d4-103">This cmdlet removes a specific received interchange control number per agreement and control number value.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b0d4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1b0d4-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b0d4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1b0d4-105">DESCRIPTION</span></span>
<span data-ttu-id="1b0d4-106">Bu cmdlet, tümleştirme hesabından alınan bir takas kontrol numarasını kaldırmak ve yinelenen numara algılama etkinleştirildiğinde B2B bağlayıcısının iletiyi işlemesi için olağanüstü durum kurtarma senaryolarında kullanılmak üzere tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="1b0d4-106">This cmdlet is meant to be used in disaster recovery scenarios to remove a received interchange control number from the integration account so that the B2B connector may process again the message when duplicate number detection is enabled.</span></span>
<span data-ttu-id="1b0d4-107">Nadir olarak, alınan değişim denetim numarası olağanüstü bir şekilde bir olağanüstü durumda ve B2B Bağlayıcısı alışverişi hatalı olarak reddetmeden önce rezerve edilebilir.</span><span class="sxs-lookup"><span data-stu-id="1b0d4-107">In rare occasions the received interchange control number may be reserved shortly before a disaster and before the B2B connector rejects the interchange as erroneous.</span></span>
<span data-ttu-id="1b0d4-108">Bu gibi durumlarda işlem, yük düzeltildikten sonra kurtarma sitesinin aynı alışverişi yeniden işlemesini etkinleştirmek isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="1b0d4-108">In such occasions the operation may want to enable the recovery site to process again the same interchange after its payload is corrected.</span></span>
<span data-ttu-id="1b0d4-109">Lütfen x12 veya Ediolgu denetim numaralarının döndürülmesini isteyip istemediğinizi belirtmek için "-AgreementType" parametresini sağlayın</span><span class="sxs-lookup"><span data-stu-id="1b0d4-109">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="1b0d4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1b0d4-110">EXAMPLES</span></span>

### <span data-ttu-id="1b0d4-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1b0d4-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
Get-AzureRmIntegrationAccountReceivedIcn : The existing recevied control number '000000641' for agreement 'X12AgreementName' is not in a valid format.
At line:1 char:1
+ Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzureRmIntegrationAccountReceivedIcn], PSInvalidOperationException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand

PS C:\> Remove-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
Get-AzureRmIntegrationAccountReceivedIcn : The session 'X12-ICN-X12AgreementName-000000641' could not be found in integration account 'accountName'.
At line:1 char:1
+ Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzureRmIntegrationAccountReceivedIcn], CloudException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand
```

<span data-ttu-id="1b0d4-112">Alınan bir x12 Interchange Control numarası alma girişimleri geçerli biçimde değil.</span><span class="sxs-lookup"><span data-stu-id="1b0d4-112">Attempts to get a received X12 interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="1b0d4-113">Alınan x12 Interchange Control numarasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1b0d4-113">Removes the received X12 interchange control number.</span></span>
<span data-ttu-id="1b0d4-114">Alınan x12 Interchange Control numarasının kaldırıldığını onaylar ve yeniden alınmaya çalışılmamıştır.</span><span class="sxs-lookup"><span data-stu-id="1b0d4-114">Confirms the received X12 interchange control number was removed by attempting to get it again.</span></span>

### <span data-ttu-id="1b0d4-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1b0d4-115">Example 2</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
Get-AzureRmIntegrationAccountReceivedIcn : The existing recevied control number '000000641' for agreement 'EdifactAgreementName' is not in a valid format.
At line:1 char:1
+ Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzureRmIntegrationAccountReceivedIcn], PSInvalidOperationException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand

PS C:\> Remove-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
Get-AzureRmIntegrationAccountReceivedIcn : The session 'Edifact-ICN-EdifactAgreementName-000000641' could not be found in integration account 'accountName'.
At line:1 char:1
+ Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzureRmIntegrationAccountReceivedIcn], CloudException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand
```

<span data-ttu-id="1b0d4-116">Alınan bir Ediolgu değişim denetimi numarası alma girişimleri, hangi içeriğin geçerli bir biçimde olmadığı.</span><span class="sxs-lookup"><span data-stu-id="1b0d4-116">Attempts to get a received Edifact interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="1b0d4-117">Alınan Ediolgu değişim denetim numarasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1b0d4-117">Removes the received Edifact interchange control number.</span></span>
<span data-ttu-id="1b0d4-118">Alınan Ediolgu değişim denetim numarasının kaldırıldığını onaylar ve yeniden alınmaya çalışılmaya çalışıyor.</span><span class="sxs-lookup"><span data-stu-id="1b0d4-118">Confirms the received Edifact interchange control number was removed by attempting to get it again.</span></span>

## <span data-ttu-id="1b0d4-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1b0d4-119">PARAMETERS</span></span>

### <span data-ttu-id="1b0d4-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="1b0d4-120">-AgreementName</span></span>
<span data-ttu-id="1b0d4-121">Tümleştirme hesabı anlaşma adı.</span><span class="sxs-lookup"><span data-stu-id="1b0d4-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="1b0d4-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="1b0d4-122">-AgreementType</span></span>
<span data-ttu-id="1b0d4-123">Tümleştirme hesabı anlaşma türü.</span><span class="sxs-lookup"><span data-stu-id="1b0d4-123">The integration account agreement type.</span></span>

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

### <span data-ttu-id="1b0d4-124">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="1b0d4-124">-ControlNumberValue</span></span>
<span data-ttu-id="1b0d4-125">Tümleştirme hesabı kontrol numarası değeri.</span><span class="sxs-lookup"><span data-stu-id="1b0d4-125">The integration account control number value.</span></span>

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

### <span data-ttu-id="1b0d4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b0d4-126">-DefaultProfile</span></span>
<span data-ttu-id="1b0d4-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1b0d4-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b0d4-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="1b0d4-128">-Name</span></span>
<span data-ttu-id="1b0d4-129">Tümleştirme hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="1b0d4-129">The integration account name.</span></span>

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

### <span data-ttu-id="1b0d4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b0d4-130">-ResourceGroupName</span></span>
<span data-ttu-id="1b0d4-131">Tümleştirme hesabı kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="1b0d4-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="1b0d4-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="1b0d4-132">-Confirm</span></span>
<span data-ttu-id="1b0d4-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1b0d4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b0d4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b0d4-134">-WhatIf</span></span>
<span data-ttu-id="1b0d4-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1b0d4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b0d4-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1b0d4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b0d4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b0d4-137">CommonParameters</span></span>
<span data-ttu-id="1b0d4-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1b0d4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b0d4-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b0d4-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b0d4-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1b0d4-140">INPUTS</span></span>

### <span data-ttu-id="1b0d4-141">System. String</span><span class="sxs-lookup"><span data-stu-id="1b0d4-141">System.String</span></span>

## <span data-ttu-id="1b0d4-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1b0d4-142">OUTPUTS</span></span>

### <span data-ttu-id="1b0d4-143">System. void</span><span class="sxs-lookup"><span data-stu-id="1b0d4-143">System.Void</span></span>

## <span data-ttu-id="1b0d4-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1b0d4-144">NOTES</span></span>

## <span data-ttu-id="1b0d4-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1b0d4-145">RELATED LINKS</span></span>

<span data-ttu-id="1b0d4-146">[Get-Azurermintegrationaccountreceivedın](./Get-AzureRmIntegrationAccountReceivedIcn.md) 
 [Set-AzureRmIntegrationAccountReceivedIcn](./Set-AzureRmIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="1b0d4-146">[Get-AzureRmIntegrationAccountReceivedIcn](./Get-AzureRmIntegrationAccountReceivedIcn.md)
[Set-AzureRmIntegrationAccountReceivedIcn](./Set-AzureRmIntegrationAccountReceivedIcn.md)</span></span>
