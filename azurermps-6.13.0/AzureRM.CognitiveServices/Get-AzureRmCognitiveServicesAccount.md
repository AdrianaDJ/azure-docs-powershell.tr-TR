---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11D5BFDF-5E5D-46B2-9F9B-A0524EFA1B42
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 3f139d4164c092f6ef57ad29d5ab9ad3eac59b56
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592788"
---
# <span data-ttu-id="83055-101">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="83055-101">Get-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="83055-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83055-102">SYNOPSIS</span></span>
<span data-ttu-id="83055-103">Bir hesap alır.</span><span class="sxs-lookup"><span data-stu-id="83055-103">Gets an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83055-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="83055-104">SYNTAX</span></span>

### <span data-ttu-id="83055-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="83055-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="83055-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="83055-106">AccountNameParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83055-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="83055-107">DESCRIPTION</span></span>
<span data-ttu-id="83055-108">**Get-Azurermöğretici Iveservicesaccount** cmdlet *'i, kaynak* grubundaki kaynak grubunda, kaynak grubunda, kaynak grubunda, sağlanan öğretici sahibi hizmet hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="83055-108">The **Get-AzureRmCognitiveServicesAccount** cmdlet gets the provisioned Cognitive Services accounts in the resource group specified by the *ResoureGroupName* parameter.</span></span>
<span data-ttu-id="83055-109">*Kaynak adı* parametresini belirtmezseniz, bu cmdlet geçerli aboneliğin tüm öğretici hizmet hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="83055-109">If you do not specify the *ResoureGroupName* parameter, this cmdlet gets all Cognitive Services accounts for the current subscription.</span></span>

## <span data-ttu-id="83055-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="83055-110">EXAMPLES</span></span>

### <span data-ttu-id="83055-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="83055-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locati
on 'WestUS'

ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WESTUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="83055-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="83055-112">PARAMETERS</span></span>

### <span data-ttu-id="83055-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83055-113">-DefaultProfile</span></span>
<span data-ttu-id="83055-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="83055-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83055-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="83055-115">-Name</span></span>
<span data-ttu-id="83055-116">Alınacak öğretici Hizmetleri hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="83055-116">Specifies the name of the Cognitive Services account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83055-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83055-117">-ResourceGroupName</span></span>
<span data-ttu-id="83055-118">Öğretici hizmetler hesabının atandığı kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="83055-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83055-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83055-119">CommonParameters</span></span>
<span data-ttu-id="83055-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="83055-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83055-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83055-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83055-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="83055-122">INPUTS</span></span>

### <span data-ttu-id="83055-123">System. String</span><span class="sxs-lookup"><span data-stu-id="83055-123">System.String</span></span>

## <span data-ttu-id="83055-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="83055-124">OUTPUTS</span></span>

### <span data-ttu-id="83055-125">Microsoft. Azure. Commands. Management. öğretici ınitialveservices. modeller. Psöğretici Iveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="83055-125">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="83055-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="83055-126">NOTES</span></span>

## <span data-ttu-id="83055-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="83055-127">RELATED LINKS</span></span>

[<span data-ttu-id="83055-128">Yeni-Azurermöğretici</span><span class="sxs-lookup"><span data-stu-id="83055-128">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="83055-129">Remove-Azurermöğretici Iveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="83055-129">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="83055-130">Set-Azurermöğretici Itiveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="83055-130">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)


