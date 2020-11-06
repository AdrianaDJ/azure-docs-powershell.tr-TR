---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: b002ca0dca3f3974af8cd05e8ae7c7babf2af486
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594006"
---
# <span data-ttu-id="ea557-101">Set-AzureRmIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="ea557-101">Set-AzureRmIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="ea557-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea557-102">SYNOPSIS</span></span>
<span data-ttu-id="ea557-103">Azure Kaynak grubundaki tümleştirme hesabı tarafından oluşturulan değişim denetim numarasını (ıCN) güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ea557-103">Updates the integration account generated interchange control number (ICN) in the Azure resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea557-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ea557-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumber <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea557-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ea557-105">DESCRIPTION</span></span>
<span data-ttu-id="ea557-106">Set-AzureRmIntegrationAccountGeneratedIcn cmdlet 'i, mevcut bir tümleştirme hesabını güncelleştirir değişim denetim numarası (ıCN)</span><span class="sxs-lookup"><span data-stu-id="ea557-106">The Set-AzureRmIntegrationAccountGeneratedIcn cmdlet updates an existing integration account generated interchange control number (ICN) and returns an object that represents the integration account generated interchange control number.</span></span>
<span data-ttu-id="ea557-107">Bu cmdlet 'i, tümleştirme hesabı oluşturulmuş değişim denetim numarasını güncelleştirmek için kullanın.</span><span class="sxs-lookup"><span data-stu-id="ea557-107">Use this cmdlet to update an integration account generated interchange control number.</span></span>
<span data-ttu-id="ea557-108">Tümleştirme hesabı adını, kaynak grubu adını ve anlaşma adını belirterek, tümleştirme hesabı tarafından oluşturulan bir değişim denetim numarasını güncelleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ea557-108">You can update an integration account generated interchange control number by specifying the integration account name, resource group name and agreement name.</span></span>
<span data-ttu-id="ea557-109">Bu komutla yeni bir tümleştirme hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="ea557-109">You cannot create a new integration account generated interchange control number with this command.</span></span>
<span data-ttu-id="ea557-110">Dinamik parametreleri kullanmak için, bunları komuta yazın veya parametre adını belirtmek için bir kısa çizgi işareti (-) yazın ve ardından kullanılabilir parametreler arasında ilerlemek için SEKME tuşuna art arda basın.</span><span class="sxs-lookup"><span data-stu-id="ea557-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ea557-111">Gerekli bir şablon parametresini kaçırırsanız cmdlet, sizden değer ister.</span><span class="sxs-lookup"><span data-stu-id="ea557-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="ea557-112">Komut satırında belirttiğiniz şablon parametre dosyası değerleri, bir şablon parametre nesnesindeki şablon parametre değerlerinden önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="ea557-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="ea557-113">Lütfen x12 veya Ediolgu denetim numaralarının döndürülmesini isteyip istemediğinizi belirtmek için "-AgreementType" parametresini sağlayın</span><span class="sxs-lookup"><span data-stu-id="ea557-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="ea557-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ea557-114">EXAMPLES</span></span>

### <span data-ttu-id="ea557-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ea557-115">Example 1</span></span>
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

<span data-ttu-id="ea557-116">Bu komut, belirli bir tümleştirme hesabı anlaşması için x12 Interchange Control numarası üretilen tümleştirme hesabını alır, değerini 100 ile artırıp güncelleştirilmiş değeri yeniden yazar.</span><span class="sxs-lookup"><span data-stu-id="ea557-116">This command gets the integration account generated X12 interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

### <span data-ttu-id="ea557-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="ea557-117">Example 2</span></span>
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

<span data-ttu-id="ea557-118">Bu komut, belirli bir tümleştirme hesabı anlaşması için Edıfactıntegrationaccountagreement Interchange için Integration hesabını alır, değerini 100 ile artırıp güncelleştirilmiş değeri geri yazar.</span><span class="sxs-lookup"><span data-stu-id="ea557-118">This command gets the integration account generated EdifactIntegrationAccountAgreement interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

## <span data-ttu-id="ea557-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ea557-119">PARAMETERS</span></span>

### <span data-ttu-id="ea557-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="ea557-120">-AgreementName</span></span>
<span data-ttu-id="ea557-121">Tümleştirme hesabı anlaşma adı.</span><span class="sxs-lookup"><span data-stu-id="ea557-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="ea557-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="ea557-122">-AgreementType</span></span>
<span data-ttu-id="ea557-123">Tümleştirme hesabı anlaşma türü.</span><span class="sxs-lookup"><span data-stu-id="ea557-123">The integration account agreement type.</span></span>

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

### <span data-ttu-id="ea557-124">-ControlNumber</span><span class="sxs-lookup"><span data-stu-id="ea557-124">-ControlNumber</span></span>
<span data-ttu-id="ea557-125">Oluşturulan denetim numarası yeni değer.</span><span class="sxs-lookup"><span data-stu-id="ea557-125">The generated control number new value.</span></span>

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

### <span data-ttu-id="ea557-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea557-126">-DefaultProfile</span></span>
<span data-ttu-id="ea557-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ea557-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea557-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="ea557-128">-Name</span></span>
<span data-ttu-id="ea557-129">Tümleştirme hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="ea557-129">The integration account name.</span></span>

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

### <span data-ttu-id="ea557-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea557-130">-ResourceGroupName</span></span>
<span data-ttu-id="ea557-131">Tümleştirme hesabı kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ea557-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="ea557-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="ea557-132">-Confirm</span></span>
<span data-ttu-id="ea557-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ea557-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea557-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea557-134">-WhatIf</span></span>
<span data-ttu-id="ea557-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ea557-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea557-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ea557-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea557-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea557-137">CommonParameters</span></span>
<span data-ttu-id="ea557-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ea557-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea557-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea557-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea557-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ea557-140">INPUTS</span></span>

### <span data-ttu-id="ea557-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ea557-141">System.String</span></span>

## <span data-ttu-id="ea557-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ea557-142">OUTPUTS</span></span>

### <span data-ttu-id="ea557-143">Microsoft. Azure. Commands. Logicuyg. Utilities. ıntegrationaccountcontrolnumber</span><span class="sxs-lookup"><span data-stu-id="ea557-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="ea557-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ea557-144">NOTES</span></span>

## <span data-ttu-id="ea557-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ea557-145">RELATED LINKS</span></span>

[<span data-ttu-id="ea557-146">Get-AzureRmIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="ea557-146">Get-AzureRmIntegrationAccountGeneratedIcn</span></span>](./Get-AzureRmIntegrationAccountGeneratedIcn.md)

