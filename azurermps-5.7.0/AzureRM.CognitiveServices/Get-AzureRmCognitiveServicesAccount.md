---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11D5BFDF-5E5D-46B2-9F9B-A0524EFA1B42
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 41d217579175de3c1de6f36b6850dfd391ca04b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591078"
---
# <span data-ttu-id="809ef-101">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="809ef-101">Get-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="809ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="809ef-102">SYNOPSIS</span></span>
<span data-ttu-id="809ef-103">Bir hesap alır.</span><span class="sxs-lookup"><span data-stu-id="809ef-103">Gets an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="809ef-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="809ef-104">SYNTAX</span></span>

### <span data-ttu-id="809ef-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="809ef-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="809ef-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="809ef-106">AccountNameParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="809ef-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="809ef-107">DESCRIPTION</span></span>
<span data-ttu-id="809ef-108">**Get-Azurermöğretici Iveservicesaccount** cmdlet *'i, kaynak* grubundaki kaynak grubunda, kaynak grubunda, kaynak grubunda, sağlanan öğretici sahibi hizmet hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="809ef-108">The **Get-AzureRmCognitiveServicesAccount** cmdlet gets the provisioned Cognitive Services accounts in the resource group specified by the *ResoureGroupName* parameter.</span></span>

<span data-ttu-id="809ef-109">*Kaynak adı* parametresini belirtmezseniz, bu cmdlet geçerli aboneliğin tüm öğretici hizmet hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="809ef-109">If you do not specify the *ResoureGroupName* parameter, this cmdlet gets all Cognitive Services accounts for the current subscription.</span></span>

## <span data-ttu-id="809ef-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="809ef-110">EXAMPLES</span></span>

## <span data-ttu-id="809ef-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="809ef-111">PARAMETERS</span></span>

### <span data-ttu-id="809ef-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="809ef-112">-DefaultProfile</span></span>
<span data-ttu-id="809ef-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="809ef-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="809ef-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="809ef-114">-Name</span></span>
<span data-ttu-id="809ef-115">Alınacak öğretici Hizmetleri hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="809ef-115">Specifies the name of the Cognitive Services account to get.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="809ef-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="809ef-116">-ResourceGroupName</span></span>
<span data-ttu-id="809ef-117">Öğretici hizmetler hesabının atandığı kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="809ef-117">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="809ef-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="809ef-118">CommonParameters</span></span>
<span data-ttu-id="809ef-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="809ef-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="809ef-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="809ef-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="809ef-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="809ef-121">INPUTS</span></span>

### <span data-ttu-id="809ef-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="809ef-122">None</span></span>
<span data-ttu-id="809ef-123">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="809ef-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="809ef-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="809ef-124">OUTPUTS</span></span>

### <span data-ttu-id="809ef-125">Microsoft. Azure. Commands. Management. öğretici ınitialveservices. modeller. Psöğretici Iveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="809ef-125">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="809ef-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="809ef-126">NOTES</span></span>

## <span data-ttu-id="809ef-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="809ef-127">RELATED LINKS</span></span>

[<span data-ttu-id="809ef-128">Yeni-Azurermöğretici</span><span class="sxs-lookup"><span data-stu-id="809ef-128">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="809ef-129">Remove-Azurermöğretici Iveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="809ef-129">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="809ef-130">Set-Azurermöğretici Itiveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="809ef-130">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)


