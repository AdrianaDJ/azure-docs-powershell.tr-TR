---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11D5BFDF-5E5D-46B2-9F9B-A0524EFA1B42
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: c4419707c9c536a21e5fdc8aa39326b02e21937c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591117"
---
# <span data-ttu-id="7b12a-101">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7b12a-101">Get-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="7b12a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b12a-102">SYNOPSIS</span></span>
<span data-ttu-id="7b12a-103">Bir hesap alır.</span><span class="sxs-lookup"><span data-stu-id="7b12a-103">Gets an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b12a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7b12a-104">SYNTAX</span></span>

### <span data-ttu-id="7b12a-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b12a-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7b12a-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b12a-106">AccountNameParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b12a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7b12a-107">DESCRIPTION</span></span>
<span data-ttu-id="7b12a-108">**Get-Azurermöğretici Iveservicesaccount** cmdlet *'i, kaynak* grubundaki kaynak grubunda, kaynak grubunda, kaynak grubunda, sağlanan öğretici sahibi hizmet hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="7b12a-108">The **Get-AzureRmCognitiveServicesAccount** cmdlet gets the provisioned Cognitive Services accounts in the resource group specified by the *ResoureGroupName* parameter.</span></span>

<span data-ttu-id="7b12a-109">*Kaynak adı* parametresini belirtmezseniz, bu cmdlet geçerli aboneliğin tüm öğretici hizmet hesaplarını alır.</span><span class="sxs-lookup"><span data-stu-id="7b12a-109">If you do not specify the *ResoureGroupName* parameter, this cmdlet gets all Cognitive Services accounts for the current subscription.</span></span>

## <span data-ttu-id="7b12a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7b12a-110">EXAMPLES</span></span>

## <span data-ttu-id="7b12a-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7b12a-111">PARAMETERS</span></span>

### <span data-ttu-id="7b12a-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="7b12a-112">-Name</span></span>
<span data-ttu-id="7b12a-113">Alınacak öğretici Hizmetleri hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b12a-113">Specifies the name of the Cognitive Services account to get.</span></span>

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

### <span data-ttu-id="7b12a-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b12a-114">-ResourceGroupName</span></span>
<span data-ttu-id="7b12a-115">Öğretici hizmetler hesabının atandığı kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b12a-115">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="7b12a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b12a-116">-DefaultProfile</span></span>
<span data-ttu-id="7b12a-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7b12a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b12a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b12a-118">CommonParameters</span></span>
<span data-ttu-id="7b12a-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7b12a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b12a-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b12a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b12a-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7b12a-121">INPUTS</span></span>

## <span data-ttu-id="7b12a-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7b12a-122">OUTPUTS</span></span>

### <span data-ttu-id="7b12a-123">Microsoft. Azure. Commands. Management. öğretici ınitialveservices. modeller. Psöğretici Iveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="7b12a-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="7b12a-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7b12a-124">NOTES</span></span>

## <span data-ttu-id="7b12a-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7b12a-125">RELATED LINKS</span></span>

[<span data-ttu-id="7b12a-126">Yeni-Azurermöğretici</span><span class="sxs-lookup"><span data-stu-id="7b12a-126">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="7b12a-127">Remove-Azurermöğretici Iveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="7b12a-127">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="7b12a-128">Set-Azurermöğretici Itiveservicesaccount</span><span class="sxs-lookup"><span data-stu-id="7b12a-128">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)


