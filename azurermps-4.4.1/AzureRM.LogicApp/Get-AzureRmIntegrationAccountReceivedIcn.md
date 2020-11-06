---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountReceivedIcn.md
ms.openlocfilehash: be42bd7d3e4a6a839182ae36d71f73377460eceb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587889"
---
# <span data-ttu-id="6fc6d-101">Get-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="6fc6d-101">Get-AzureRmIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="6fc6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fc6d-102">SYNOPSIS</span></span>
<span data-ttu-id="6fc6d-103">Bu cmdlet, anlaşma ve denetim numarası değeri başına alınan belirli bir takas denetim numarasını alır.</span><span class="sxs-lookup"><span data-stu-id="6fc6d-103">This cmdlet retrieves a specific received interchange control number per agreement and control number value.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fc6d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6fc6d-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6fc6d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6fc6d-105">DESCRIPTION</span></span>
<span data-ttu-id="6fc6d-106">Bu cmdlet, alınan bir değişim denetim numarasının varlığını doğrulamak ve isteğe bağlı olarak bu varlığı Remove-AzureRmIntegrationAccountReceivedIcn ile kaldırmak için olağanüstü durum kurtarma senaryolarında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6fc6d-106">This cmdlet is meant to be used in disaster recovery scenarios to validate the presence of a received interchange control number and optionally to remove that entity with Remove-AzureRmIntegrationAccountReceivedIcn.</span></span>
<span data-ttu-id="6fc6d-107">Lütfen x12 veya Ediolgu denetim numaralarının döndürülmesini isteyip istemediğinizi belirtmek için "-AgreementType" parametresini sağlayın</span><span class="sxs-lookup"><span data-stu-id="6fc6d-107">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="6fc6d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6fc6d-108">EXAMPLES</span></span>

### <span data-ttu-id="6fc6d-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6fc6d-109">Example 1</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="6fc6d-110">Bu komut, x12 tümleştirme hesabını anlaşma adına ve denetim numarası değerine göre değişim denetim numarasını almıştır.</span><span class="sxs-lookup"><span data-stu-id="6fc6d-110">This command gets the X12 integration account received interchange control number by agreement name and control number value.</span></span>

### <span data-ttu-id="6fc6d-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="6fc6d-111">Example 2</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="6fc6d-112">Bu komut, anlaşma adına ve denetim numarası değerine göre Edıkıntegration hesabını alınan değişim denetim numarasını alır.</span><span class="sxs-lookup"><span data-stu-id="6fc6d-112">This command gets the Edifact integration account received interchange control number by agreement name and control number value.</span></span>

## <span data-ttu-id="6fc6d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6fc6d-113">PARAMETERS</span></span>

### <span data-ttu-id="6fc6d-114">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="6fc6d-114">-AgreementName</span></span>
<span data-ttu-id="6fc6d-115">Tümleştirme hesabı anlaşma adı.</span><span class="sxs-lookup"><span data-stu-id="6fc6d-115">The integration account agreement name.</span></span>

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

### <span data-ttu-id="6fc6d-116">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="6fc6d-116">-ControlNumberValue</span></span>
<span data-ttu-id="6fc6d-117">Tümleştirme hesabı kontrol numarası değeri.</span><span class="sxs-lookup"><span data-stu-id="6fc6d-117">The integration account control number value.</span></span>

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

### <span data-ttu-id="6fc6d-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="6fc6d-118">-Name</span></span>
<span data-ttu-id="6fc6d-119">Tümleştirme hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="6fc6d-119">The integration account name.</span></span>

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

### <span data-ttu-id="6fc6d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fc6d-120">-ResourceGroupName</span></span>
<span data-ttu-id="6fc6d-121">Tümleştirme hesabı kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="6fc6d-121">The integration account resource group name.</span></span>

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

### <span data-ttu-id="6fc6d-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="6fc6d-122">-AgreementType</span></span>
<span data-ttu-id="6fc6d-123">Tümleştirme hesabı anlaşma türü.</span><span class="sxs-lookup"><span data-stu-id="6fc6d-123">The integration account agreement type.</span></span>

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

### <span data-ttu-id="6fc6d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fc6d-124">-DefaultProfile</span></span>
<span data-ttu-id="6fc6d-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6fc6d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fc6d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fc6d-126">CommonParameters</span></span>
<span data-ttu-id="6fc6d-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6fc6d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fc6d-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fc6d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fc6d-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6fc6d-129">INPUTS</span></span>

### <span data-ttu-id="6fc6d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6fc6d-130">System.String</span></span>

## <span data-ttu-id="6fc6d-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6fc6d-131">OUTPUTS</span></span>

### <span data-ttu-id="6fc6d-132">Microsoft. Azure. Commands. Logicuyg. Utilities. ıntegrationaccountclient + ıntegrationaccountcontrolnumber</span><span class="sxs-lookup"><span data-stu-id="6fc6d-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountClient+IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="6fc6d-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6fc6d-133">NOTES</span></span>

## <span data-ttu-id="6fc6d-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6fc6d-134">RELATED LINKS</span></span>

[<span data-ttu-id="6fc6d-135">Set-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="6fc6d-135">Set-AzureRmIntegrationAccountReceivedIcn</span></span>](./Set-AzureRmIntegrationAccountReceivedIcn.md)

[<span data-ttu-id="6fc6d-136">Remove-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="6fc6d-136">Remove-AzureRmIntegrationAccountReceivedIcn</span></span>](./Remove-AzureRmIntegrationAccountReceivedIcn.md)
