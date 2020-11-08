---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: d7c6e5cfc1462e0ae807c9cdddb2d743a7608738
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280166"
---
# <span data-ttu-id="75611-101">Get-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="75611-101">Get-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="75611-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75611-102">SYNOPSIS</span></span>
<span data-ttu-id="75611-103">Bu cmdlet, anlaşma ve denetim numarası değeri başına alınan belirli bir takas denetim numarasını alır.</span><span class="sxs-lookup"><span data-stu-id="75611-103">This cmdlet retrieves a specific received interchange control number per agreement and control number value.</span></span>

## <span data-ttu-id="75611-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="75611-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="75611-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="75611-105">DESCRIPTION</span></span>
<span data-ttu-id="75611-106">Bu cmdlet, alınan bir değişim denetim numarasının varlığını doğrulamak ve isteğe bağlı olarak bu varlığı Remove-Azıntegrationaccountreceivedıp ile kaldırmak için olağanüstü durum kurtarma senaryolarında kullanılmak üzere tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="75611-106">This cmdlet is meant to be used in disaster recovery scenarios to validate the presence of a received interchange control number and optionally to remove that entity with Remove-AzIntegrationAccountReceivedIcn.</span></span>
<span data-ttu-id="75611-107">Lütfen x12 veya Ediolgu denetim numaralarının döndürülmesini isteyip istemediğinizi belirtmek için "-AgreementType" parametresini sağlayın</span><span class="sxs-lookup"><span data-stu-id="75611-107">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="75611-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="75611-108">EXAMPLES</span></span>

### <span data-ttu-id="75611-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="75611-109">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="75611-110">Bu komut, x12 tümleştirme hesabını anlaşma adına ve denetim numarası değerine göre değişim denetim numarasını almıştır.</span><span class="sxs-lookup"><span data-stu-id="75611-110">This command gets the X12 integration account received interchange control number by agreement name and control number value.</span></span>

### <span data-ttu-id="75611-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="75611-111">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="75611-112">Bu komut, anlaşma adına ve denetim numarası değerine göre Edıkıntegration hesabını alınan değişim denetim numarasını alır.</span><span class="sxs-lookup"><span data-stu-id="75611-112">This command gets the Edifact integration account received interchange control number by agreement name and control number value.</span></span>

## <span data-ttu-id="75611-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="75611-113">PARAMETERS</span></span>

### <span data-ttu-id="75611-114">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="75611-114">-AgreementName</span></span>
<span data-ttu-id="75611-115">Tümleştirme hesabı anlaşma adı.</span><span class="sxs-lookup"><span data-stu-id="75611-115">The integration account agreement name.</span></span>

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

### <span data-ttu-id="75611-116">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="75611-116">-AgreementType</span></span>
<span data-ttu-id="75611-117">Tümleştirme hesabı anlaşma türü.</span><span class="sxs-lookup"><span data-stu-id="75611-117">The integration account agreement type.</span></span>

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

### <span data-ttu-id="75611-118">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="75611-118">-ControlNumberValue</span></span>
<span data-ttu-id="75611-119">Tümleştirme hesabı kontrol numarası değeri.</span><span class="sxs-lookup"><span data-stu-id="75611-119">The integration account control number value.</span></span>

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

### <span data-ttu-id="75611-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75611-120">-DefaultProfile</span></span>
<span data-ttu-id="75611-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="75611-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75611-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="75611-122">-Name</span></span>
<span data-ttu-id="75611-123">Tümleştirme hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="75611-123">The integration account name.</span></span>

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

### <span data-ttu-id="75611-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75611-124">-ResourceGroupName</span></span>
<span data-ttu-id="75611-125">Tümleştirme hesabı kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="75611-125">The integration account resource group name.</span></span>

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

### <span data-ttu-id="75611-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75611-126">CommonParameters</span></span>
<span data-ttu-id="75611-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="75611-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75611-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75611-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75611-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="75611-129">INPUTS</span></span>

### <span data-ttu-id="75611-130">System. String</span><span class="sxs-lookup"><span data-stu-id="75611-130">System.String</span></span>

## <span data-ttu-id="75611-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="75611-131">OUTPUTS</span></span>

### <span data-ttu-id="75611-132">Microsoft. Azure. Commands. Logicuyg. Utilities. ıntegrationaccountcontrolnumber</span><span class="sxs-lookup"><span data-stu-id="75611-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="75611-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="75611-133">NOTES</span></span>

## <span data-ttu-id="75611-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="75611-134">RELATED LINKS</span></span>

[<span data-ttu-id="75611-135">Set-az</span><span class="sxs-lookup"><span data-stu-id="75611-135">Set-AzIntegrationAccountReceivedIcn</span></span>](./Set-AzIntegrationAccountReceivedIcn.md)

[<span data-ttu-id="75611-136">Remove-Azıntegrationaccountreceivedın</span><span class="sxs-lookup"><span data-stu-id="75611-136">Remove-AzIntegrationAccountReceivedIcn</span></span>](./Remove-AzIntegrationAccountReceivedIcn.md)
