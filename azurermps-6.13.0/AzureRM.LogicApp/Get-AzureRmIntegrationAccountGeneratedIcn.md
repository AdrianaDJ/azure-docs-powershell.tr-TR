---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: 0f35bf23f06d98e4d9de2e249565e10f23498295
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593238"
---
# <span data-ttu-id="e30df-101">Get-AzureRmIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="e30df-101">Get-AzureRmIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="e30df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e30df-102">SYNOPSIS</span></span>
<span data-ttu-id="e30df-103">Bu cmdlet, anlaşma başına oluşturulan değişim denetim numarasının geçerli değerini alır.</span><span class="sxs-lookup"><span data-stu-id="e30df-103">This cmdlet retrieves the current value of the generated interchange control number per agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e30df-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e30df-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> [-AgreementName <String>]
 [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e30df-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e30df-105">DESCRIPTION</span></span>
<span data-ttu-id="e30df-106">Bu cmdlet, küme-AzureRmIntegrationAccountGeneratedIcn ile artan bir değeri geri yazmak için, olağanüstü durum kurtarma senaryolarında kullanılacak</span><span class="sxs-lookup"><span data-stu-id="e30df-106">This cmdlet is meant to be used in disaster recovery scenarios to retrieve the current value of the generated interchange control number so to write back an increased value with Set-AzureRmIntegrationAccountGeneratedIcn.</span></span>
<span data-ttu-id="e30df-107">Etkin bölgede olağanüstü durum oluştuğu için, pasif bölgeye çoğaltılmamış olan sayıların yinelenen takas denetim numaralarını önlemek için, değişim denetim numarası artırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="e30df-107">The interchange control number should be increased to avoid duplicate interchange control numbers for the numbers that could not yet be replicated to the passive region when the disaster happened in the active region.</span></span>
<span data-ttu-id="e30df-108">Lütfen x12 veya Ediolgu denetim numaralarının döndürülmesini isteyip istemediğinizi belirtmek için "-AgreementType" parametresini sağlayın</span><span class="sxs-lookup"><span data-stu-id="e30df-108">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="e30df-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e30df-109">EXAMPLES</span></span>

### <span data-ttu-id="e30df-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e30df-110">Example 1</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="e30df-111">Bu komut, anlaşma hesabını, anlaşma adına göre x12 Interchange Control numarasıyla üretilen tümleştirme hesabını alır.</span><span class="sxs-lookup"><span data-stu-id="e30df-111">This command gets the integration account generated X12 interchange control number by agreement name.</span></span> <span data-ttu-id="e30df-112">Sözleşmenin belirtilen "x12" türünde olduğundan emin olun</span><span class="sxs-lookup"><span data-stu-id="e30df-112">Please make sure agreement specified is of type "X12"</span></span>

### <span data-ttu-id="e30df-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e30df-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="e30df-114">Bu komut, tümleştirme hesabını, anlaşma adına göre oluşturulmuş Edıbulınterchange denetim numarasını alır.</span><span class="sxs-lookup"><span data-stu-id="e30df-114">This command gets the integration account generated Edifact interchange control number by agreement name.</span></span> <span data-ttu-id="e30df-115">Sözleşmenin belirtilen "Ediolgu" türünde olduğundan emin olun</span><span class="sxs-lookup"><span data-stu-id="e30df-115">Please make sure agreement specified is of type "Edifact"</span></span>

### <span data-ttu-id="e30df-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="e30df-116">Example 3</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1"
ControlNumber            : 1000
ControlNumberChangedTime : 2/22/2017 8:05:41 PM
AgreementName            : X12IntegrationAccountAgreement1
IsMessageProcessingFailed:

ControlNumber            : 1000
ControlNumberChangedTime : 2/22/2017 8:05:41 PM
AgreementName            : X12IntegrationAccountAgreement2
IsMessageProcessingFailed:

ControlNumber            : No generated control number was found for this agreement.
ControlNumberChangedTime : 1/1/0001 12:00:00 AM
AgreementName            : X12IntegrationAccountAgreement3
IsMessageProcessingFailed:
```

<span data-ttu-id="e30df-117">Bu komut, tüm oluşturulmuş x12 değişim denetim numaralarını tümleştirme hesap adıyla alır.</span><span class="sxs-lookup"><span data-stu-id="e30df-117">This command gets all the generated X12 interchange control numbers by integration account name.</span></span>

## <span data-ttu-id="e30df-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e30df-118">PARAMETERS</span></span>

### <span data-ttu-id="e30df-119">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="e30df-119">-AgreementName</span></span>
<span data-ttu-id="e30df-120">Tümleştirme hesabı anlaşma adı.</span><span class="sxs-lookup"><span data-stu-id="e30df-120">The integration account agreement name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e30df-121">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="e30df-121">-AgreementType</span></span>
<span data-ttu-id="e30df-122">Tümleştirme hesabı anlaşma türü.</span><span class="sxs-lookup"><span data-stu-id="e30df-122">The integration account agreement type.</span></span>

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

### <span data-ttu-id="e30df-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e30df-123">-DefaultProfile</span></span>
<span data-ttu-id="e30df-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e30df-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e30df-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="e30df-125">-Name</span></span>
<span data-ttu-id="e30df-126">Tümleştirme hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="e30df-126">The integration account name.</span></span>

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

### <span data-ttu-id="e30df-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e30df-127">-ResourceGroupName</span></span>
<span data-ttu-id="e30df-128">Tümleştirme hesabı kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e30df-128">The integration account resource group name.</span></span>

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

### <span data-ttu-id="e30df-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e30df-129">CommonParameters</span></span>
<span data-ttu-id="e30df-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e30df-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e30df-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e30df-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e30df-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e30df-132">INPUTS</span></span>

### <span data-ttu-id="e30df-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e30df-133">System.String</span></span>

## <span data-ttu-id="e30df-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e30df-134">OUTPUTS</span></span>

### <span data-ttu-id="e30df-135">Microsoft. Azure. Commands. Logicuyg. Utilities. ıntegrationaccountcontrolnumber</span><span class="sxs-lookup"><span data-stu-id="e30df-135">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="e30df-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e30df-136">NOTES</span></span>

## <span data-ttu-id="e30df-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e30df-137">RELATED LINKS</span></span>

[<span data-ttu-id="e30df-138">Set-AzureRmIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="e30df-138">Set-AzureRmIntegrationAccountGeneratedIcn</span></span>](./Set-AzureRmIntegrationAccountGeneratedIcn.md)
