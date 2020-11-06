---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountReceivedIcn.md
ms.openlocfilehash: d3f5b8a00bed15f7b5fa36fc0bd1a016517eeb89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592476"
---
# <span data-ttu-id="570b6-101">Get-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="570b6-101">Get-AzureRmIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="570b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="570b6-102">SYNOPSIS</span></span>
<span data-ttu-id="570b6-103">Bu cmdlet, anlaşma ve denetim numarası değeri başına alınan belirli bir takas denetim numarasını alır.</span><span class="sxs-lookup"><span data-stu-id="570b6-103">This cmdlet retrieves a specific received interchange control number per agreement and control number value.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="570b6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="570b6-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="570b6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="570b6-105">DESCRIPTION</span></span>
<span data-ttu-id="570b6-106">Bu cmdlet, alınan bir değişim denetim numarasının varlığını doğrulamak ve isteğe bağlı olarak bu varlığı Remove-AzureRmIntegrationAccountReceivedIcn ile kaldırmak için olağanüstü durum kurtarma senaryolarında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="570b6-106">This cmdlet is meant to be used in disaster recovery scenarios to validate the presence of a received interchange control number and optionally to remove that entity with Remove-AzureRmIntegrationAccountReceivedIcn.</span></span>
<span data-ttu-id="570b6-107">Lütfen x12 veya Ediolgu denetim numaralarının döndürülmesini isteyip istemediğinizi belirtmek için "-AgreementType" parametresini sağlayın</span><span class="sxs-lookup"><span data-stu-id="570b6-107">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="570b6-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="570b6-108">EXAMPLES</span></span>

### <span data-ttu-id="570b6-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="570b6-109">Example 1</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="570b6-110">Bu komut, x12 tümleştirme hesabını anlaşma adına ve denetim numarası değerine göre değişim denetim numarasını almıştır.</span><span class="sxs-lookup"><span data-stu-id="570b6-110">This command gets the X12 integration account received interchange control number by agreement name and control number value.</span></span>

### <span data-ttu-id="570b6-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="570b6-111">Example 2</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="570b6-112">Bu komut, anlaşma adına ve denetim numarası değerine göre Edıkıntegration hesabını alınan değişim denetim numarasını alır.</span><span class="sxs-lookup"><span data-stu-id="570b6-112">This command gets the Edifact integration account received interchange control number by agreement name and control number value.</span></span>

## <span data-ttu-id="570b6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="570b6-113">PARAMETERS</span></span>

### <span data-ttu-id="570b6-114">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="570b6-114">-AgreementName</span></span>
<span data-ttu-id="570b6-115">Tümleştirme hesabı anlaşma adı.</span><span class="sxs-lookup"><span data-stu-id="570b6-115">The integration account agreement name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="570b6-116">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="570b6-116">-AgreementType</span></span>
<span data-ttu-id="570b6-117">Tümleştirme hesabı anlaşma türü.</span><span class="sxs-lookup"><span data-stu-id="570b6-117">The integration account agreement type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: MessageType
Accepted values: X12, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="570b6-118">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="570b6-118">-ControlNumberValue</span></span>
<span data-ttu-id="570b6-119">Tümleştirme hesabı kontrol numarası değeri.</span><span class="sxs-lookup"><span data-stu-id="570b6-119">The integration account control number value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="570b6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="570b6-120">-DefaultProfile</span></span>
<span data-ttu-id="570b6-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="570b6-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="570b6-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="570b6-122">-Name</span></span>
<span data-ttu-id="570b6-123">Tümleştirme hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="570b6-123">The integration account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="570b6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="570b6-124">-ResourceGroupName</span></span>
<span data-ttu-id="570b6-125">Tümleştirme hesabı kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="570b6-125">The integration account resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="570b6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="570b6-126">CommonParameters</span></span>
<span data-ttu-id="570b6-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="570b6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="570b6-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="570b6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="570b6-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="570b6-129">INPUTS</span></span>

### <span data-ttu-id="570b6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="570b6-130">System.String</span></span>

## <span data-ttu-id="570b6-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="570b6-131">OUTPUTS</span></span>

### <span data-ttu-id="570b6-132">Microsoft. Azure. Commands. Logicuyg. Utilities. ıntegrationaccountclient + ıntegrationaccountcontrolnumber</span><span class="sxs-lookup"><span data-stu-id="570b6-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountClient+IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="570b6-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="570b6-133">NOTES</span></span>

## <span data-ttu-id="570b6-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="570b6-134">RELATED LINKS</span></span>

[<span data-ttu-id="570b6-135">Set-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="570b6-135">Set-AzureRmIntegrationAccountReceivedIcn</span></span>](./Set-AzureRmIntegrationAccountReceivedIcn.md)

[<span data-ttu-id="570b6-136">Remove-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="570b6-136">Remove-AzureRmIntegrationAccountReceivedIcn</span></span>](./Remove-AzureRmIntegrationAccountReceivedIcn.md)
