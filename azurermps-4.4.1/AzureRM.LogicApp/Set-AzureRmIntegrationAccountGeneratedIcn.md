---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: dd133b2a0d982cb2017651ff86dcf3a846009c2e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763709"
---
# <span data-ttu-id="f3f12-101">Set-AzureRmIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="f3f12-101">Set-AzureRmIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="f3f12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3f12-102">SYNOPSIS</span></span>
<span data-ttu-id="f3f12-103">Azure Kaynak grubundaki tümleştirme hesabı tarafından oluşturulan değişim denetim numarasını (ıCN) güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f3f12-103">Updates the integration account generated interchange control number (ICN) in the Azure resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3f12-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f3f12-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumber <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3f12-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f3f12-105">DESCRIPTION</span></span>
<span data-ttu-id="f3f12-106">Set-AzureRmIntegrationAccountGeneratedIcn cmdlet 'i, mevcut bir tümleştirme hesabını güncelleştirir değişim denetim numarası (ıCN)</span><span class="sxs-lookup"><span data-stu-id="f3f12-106">The Set-AzureRmIntegrationAccountGeneratedIcn cmdlet updates an existing integration account generated interchange control number (ICN) and returns an object that represents the integration account generated interchange control number.</span></span>
<span data-ttu-id="f3f12-107">Bu cmdlet 'i, tümleştirme hesabı oluşturulmuş değişim denetim numarasını güncelleştirmek için kullanın.</span><span class="sxs-lookup"><span data-stu-id="f3f12-107">Use this cmdlet to update an integration account generated interchange control number.</span></span>
<span data-ttu-id="f3f12-108">Tümleştirme hesabı adını, kaynak grubu adını ve anlaşma adını belirterek, tümleştirme hesabı tarafından oluşturulan bir değişim denetim numarasını güncelleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f3f12-108">You can update an integration account generated interchange control number by specifying the integration account name, resource group name and agreement name.</span></span>
<span data-ttu-id="f3f12-109">Bu komutla yeni bir tümleştirme hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="f3f12-109">You cannot create a new integration account generated interchange control number with this command.</span></span>
<span data-ttu-id="f3f12-110">Dinamik parametreleri kullanmak için, bunları komuta yazın veya parametre adını belirtmek için bir kısa çizgi işareti (-) yazın ve ardından kullanılabilir parametreler arasında ilerlemek için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="f3f12-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f3f12-111">Gerekli bir şablon parametresini kaçırırsanız cmdlet, sizden değer ister.</span><span class="sxs-lookup"><span data-stu-id="f3f12-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="f3f12-112">Komut satırında belirttiğiniz şablon parametre dosyası değerleri, bir şablon parametre nesnesindeki şablon parametre değerlerinden önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="f3f12-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="f3f12-113">Lütfen x12 veya Ediolgu denetim numaralarının döndürülmesini isteyip istemediğinizi belirtmek için "-AgreementType" parametresini sağlayın</span><span class="sxs-lookup"><span data-stu-id="f3f12-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="f3f12-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f3f12-114">EXAMPLES</span></span>

### <span data-ttu-id="f3f12-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f3f12-115">Example 1</span></span>
```
PS C:\> $resourceGroup.ResourceGroupName = "ResourceGroup1"
PS C:\> $integrationAccountName = "IntegrationAccount1"
PS C:\> $integrationAccountAgreementName = "X12IntegrationAccountAgreement"
PS C:\> $initialControlNumber = Get-AzureRmIntegrationAccountGeneratedIcn -AgreementType X12 -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName
PS C:\> $incrementedControlNumberValue = [convert]::ToString([convert]::ToInt32($initialControlNumber.ControlNumber, 10) + 100, 10)
PS C:\> Set-AzureRmIntegrationAccountGeneratedIcn -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName -ControlNumber $incrementedControlNumberValue
ControlNumber            : 1100
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="f3f12-116">Bu komut, belirli bir tümleştirme hesabı anlaşması için x12 Interchange Control numarası üretilen tümleştirme hesabını alır, değerini 100 ile artırıp güncelleştirilmiş değeri yeniden yazar.</span><span class="sxs-lookup"><span data-stu-id="f3f12-116">This command gets the integration account generated X12 interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

### <span data-ttu-id="f3f12-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="f3f12-117">Example 2</span></span>
```
PS C:\> $resourceGroup.ResourceGroupName = "ResourceGroup1"
PS C:\> $integrationAccountName = "IntegrationAccount1"
PS C:\> $integrationAccountAgreementName = "EdifactIntegrationAccountAgreement"
PS C:\> $initialControlNumber = Get-AzureRmIntegrationAccountGeneratedIcn -AgreementType EdifactIntegrationAccountAgreement -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName
PS C:\> $incrementedControlNumberValue = [convert]::ToString([convert]::ToInt32($initialControlNumber.ControlNumber, 10) + 100, 10)
PS C:\> Set-AzureRmIntegrationAccountGeneratedIcn -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName -ControlNumber $incrementedControlNumberValue
ControlNumber            : 1100
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="f3f12-118">Bu komut, belirli bir tümleştirme hesabı anlaşması için Edıfactıntegrationaccountagreement Interchange için Integration hesabını alır, değerini 100 ile artırıp güncelleştirilmiş değeri geri yazar.</span><span class="sxs-lookup"><span data-stu-id="f3f12-118">This command gets the integration account generated EdifactIntegrationAccountAgreement interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

## <span data-ttu-id="f3f12-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f3f12-119">PARAMETERS</span></span>

### <span data-ttu-id="f3f12-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="f3f12-120">-AgreementName</span></span>
<span data-ttu-id="f3f12-121">Tümleştirme hesabı anlaşma adı.</span><span class="sxs-lookup"><span data-stu-id="f3f12-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="f3f12-122">-ControlNumber</span><span class="sxs-lookup"><span data-stu-id="f3f12-122">-ControlNumber</span></span>
<span data-ttu-id="f3f12-123">Oluşturulan denetim numarası yeni değer.</span><span class="sxs-lookup"><span data-stu-id="f3f12-123">The generated control number new value.</span></span>

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

### <span data-ttu-id="f3f12-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="f3f12-124">-Name</span></span>
<span data-ttu-id="f3f12-125">Tümleştirme hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="f3f12-125">The integration account name.</span></span>

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

### <span data-ttu-id="f3f12-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3f12-126">-ResourceGroupName</span></span>
<span data-ttu-id="f3f12-127">Tümleştirme hesabı kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f3f12-127">The integration account resource group name.</span></span>

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

### <span data-ttu-id="f3f12-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="f3f12-128">-Confirm</span></span>
<span data-ttu-id="f3f12-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f3f12-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3f12-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3f12-130">-WhatIf</span></span>
<span data-ttu-id="f3f12-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f3f12-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3f12-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f3f12-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3f12-133">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="f3f12-133">-AgreementType</span></span>
<span data-ttu-id="f3f12-134">Tümleştirme hesabı anlaşma türü.</span><span class="sxs-lookup"><span data-stu-id="f3f12-134">The integration account agreement type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MessageType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3f12-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3f12-135">-DefaultProfile</span></span>
<span data-ttu-id="f3f12-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f3f12-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3f12-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3f12-137">CommonParameters</span></span>
<span data-ttu-id="f3f12-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f3f12-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3f12-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3f12-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3f12-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f3f12-140">INPUTS</span></span>

### <span data-ttu-id="f3f12-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f3f12-141">System.String</span></span>

## <span data-ttu-id="f3f12-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f3f12-142">OUTPUTS</span></span>

### <span data-ttu-id="f3f12-143">Microsoft. Azure. Commands. Logicuyg. Utilities. ıntegrationaccountclient + ıntegrationaccountcontrolnumber</span><span class="sxs-lookup"><span data-stu-id="f3f12-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountClient+IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="f3f12-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f3f12-144">NOTES</span></span>

## <span data-ttu-id="f3f12-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f3f12-145">RELATED LINKS</span></span>

[<span data-ttu-id="f3f12-146">Get-AzureRmIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="f3f12-146">Get-AzureRmIntegrationAccountGeneratedIcn</span></span>](./Get-AzureRmIntegrationAccountGeneratedIcn.md)

