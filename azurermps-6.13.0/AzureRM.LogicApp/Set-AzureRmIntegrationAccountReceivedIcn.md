---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 5f25ec9f3b180f6bb0379b399cdbf1a96f9d1f30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594004"
---
# <span data-ttu-id="a5f0a-101">Set-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="a5f0a-101">Set-AzureRmIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="a5f0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5f0a-102">SYNOPSIS</span></span>
<span data-ttu-id="a5f0a-103">Azure Kaynak grubunda, tümleştirme hesabını alınan değişim denetim numarasını (ıCN) güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a5f0a-103">Updates the integration account received interchange control number (ICN) in the Azure resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5f0a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a5f0a-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> -IsMessageProcessingFailed <Boolean> [-AgreementType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5f0a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a5f0a-105">DESCRIPTION</span></span>
<span data-ttu-id="a5f0a-106">Set-AzureRmIntegrationAccountGeneratedIcn cmdlet 'i, var olan bir tümleştirme hesabını güncelleştirme değişim denetim numarası (ıCN) güncelleştirir ve tümleştirme hesabı aldı değişim denetim numarasını temsil eder.</span><span class="sxs-lookup"><span data-stu-id="a5f0a-106">The Set-AzureRmIntegrationAccountGeneratedIcn cmdlet updates an existing integration account received interchange control number (ICN) and returns an object that represents the integration account received interchange control number.</span></span>
<span data-ttu-id="a5f0a-107">Tümleştirme hesabı alındı değişim denetim numarasının ileti işleme durumunu güncelleştirmek için bu cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="a5f0a-107">Use this cmdlet to update an integration account received interchange control number's message processing status.</span></span>
<span data-ttu-id="a5f0a-108">Tümleştirme hesabı adını, kaynak grubu adını, anlaşma adını, denetim numarası değerini ve ileti işleme durumunu belirterek, alınan değişim denetim numarasını güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a5f0a-108">You can update an integration account received interchange control number by specifying the integration account name, resource group name, agreement name, control number value and message processing status.</span></span>
<span data-ttu-id="a5f0a-109">Bu komutla yeni bir tümleştirme hesabı için değişim denetim numarası alındı.</span><span class="sxs-lookup"><span data-stu-id="a5f0a-109">You cannot create a new integration account received interchange control number with this command.</span></span>
<span data-ttu-id="a5f0a-110">Dinamik parametreleri kullanmak için, bunları komuta yazın veya parametre adını belirtmek için bir kısa çizgi işareti (-) yazın ve ardından kullanılabilir parametreler arasında ilerlemek için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="a5f0a-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a5f0a-111">Gerekli bir şablon parametresini kaçırırsanız cmdlet, sizden değer ister.</span><span class="sxs-lookup"><span data-stu-id="a5f0a-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="a5f0a-112">Komut satırında belirttiğiniz şablon parametre dosyası değerleri, bir şablon parametre nesnesindeki şablon parametre değerlerinden önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="a5f0a-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="a5f0a-113">Lütfen x12 veya Ediolgu denetim numaralarının döndürülmesini isteyip istemediğinizi belirtmek için "-AgreementType" parametresini sağlayın</span><span class="sxs-lookup"><span data-stu-id="a5f0a-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="a5f0a-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a5f0a-114">EXAMPLES</span></span>

### <span data-ttu-id="a5f0a-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a5f0a-115">Example 1</span></span>
```
PS C:\> Set-AzureRmIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="a5f0a-116">Bu komut, belirli bir tümleştirme hesabı anlaşması için x12 Interchange Control numarası alınan tümleştirme hesabını güncelleştirir ve ileti işleme durumuyla değer başarısız oldu.</span><span class="sxs-lookup"><span data-stu-id="a5f0a-116">This command updates the integration account received X12 interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

### <span data-ttu-id="a5f0a-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a5f0a-117">Example 2</span></span>
```
PS C:\> Set-AzureRmIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="a5f0a-118">Bu komut, belirli bir tümleştirme hesabı sözleşmesinin, ileti işleme durumu olan değerin Edıma değişimi denetim numarasını almıştır.</span><span class="sxs-lookup"><span data-stu-id="a5f0a-118">This command updates the integration account received Edifact interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

## <span data-ttu-id="a5f0a-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a5f0a-119">PARAMETERS</span></span>

### <span data-ttu-id="a5f0a-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="a5f0a-120">-AgreementName</span></span>
<span data-ttu-id="a5f0a-121">Tümleştirme hesabı anlaşma adı.</span><span class="sxs-lookup"><span data-stu-id="a5f0a-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="a5f0a-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="a5f0a-122">-AgreementType</span></span>
<span data-ttu-id="a5f0a-123">Tümleştirme hesabı anlaşma türü (x12 veya Ediolgu).</span><span class="sxs-lookup"><span data-stu-id="a5f0a-123">The integration account agreement type (X12 or Edifact).</span></span>

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

### <span data-ttu-id="a5f0a-124">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="a5f0a-124">-ControlNumberValue</span></span>
<span data-ttu-id="a5f0a-125">Tümleştirme hesabı kontrol numarası değeri.</span><span class="sxs-lookup"><span data-stu-id="a5f0a-125">The integration account control number value.</span></span>

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

### <span data-ttu-id="a5f0a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5f0a-126">-DefaultProfile</span></span>
<span data-ttu-id="a5f0a-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a5f0a-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5f0a-128">-Ismessageprocessingbaşarısız</span><span class="sxs-lookup"><span data-stu-id="a5f0a-128">-IsMessageProcessingFailed</span></span>
<span data-ttu-id="a5f0a-129">Alınan ileti işleme durumu.</span><span class="sxs-lookup"><span data-stu-id="a5f0a-129">The received message processing status.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5f0a-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="a5f0a-130">-Name</span></span>
<span data-ttu-id="a5f0a-131">Tümleştirme hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="a5f0a-131">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5f0a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5f0a-132">-ResourceGroupName</span></span>
<span data-ttu-id="a5f0a-133">Tümleştirme hesabı kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="a5f0a-133">The integration account resource group name.</span></span>

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

### <span data-ttu-id="a5f0a-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="a5f0a-134">-Confirm</span></span>
<span data-ttu-id="a5f0a-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a5f0a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5f0a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5f0a-136">-WhatIf</span></span>
<span data-ttu-id="a5f0a-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a5f0a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5f0a-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a5f0a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5f0a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5f0a-139">CommonParameters</span></span>
<span data-ttu-id="a5f0a-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a5f0a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5f0a-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5f0a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5f0a-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a5f0a-142">INPUTS</span></span>

### <span data-ttu-id="a5f0a-143">System. String</span><span class="sxs-lookup"><span data-stu-id="a5f0a-143">System.String</span></span>

## <span data-ttu-id="a5f0a-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a5f0a-144">OUTPUTS</span></span>

### <span data-ttu-id="a5f0a-145">Microsoft. Azure. Commands. Logicuyg. Utilities. ıntegrationaccountcontrolnumber</span><span class="sxs-lookup"><span data-stu-id="a5f0a-145">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="a5f0a-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a5f0a-146">NOTES</span></span>

## <span data-ttu-id="a5f0a-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a5f0a-147">RELATED LINKS</span></span>

<span data-ttu-id="a5f0a-148">[Get-Azurermintegrationaccountreceivedın](./Get-AzureRmIntegrationAccountReceivedIcn.md) 
 [Remove-AzureRmIntegrationAccountReceivedIcn](./Remove-AzureRmIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="a5f0a-148">[Get-AzureRmIntegrationAccountReceivedIcn](./Get-AzureRmIntegrationAccountReceivedIcn.md)
[Remove-AzureRmIntegrationAccountReceivedIcn](./Remove-AzureRmIntegrationAccountReceivedIcn.md)</span></span>
