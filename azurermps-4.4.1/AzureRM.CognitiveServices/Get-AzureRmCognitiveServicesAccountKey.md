---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 73B1EB7E-568E-44E8-993A-91678B7D8AEE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountKey.md
ms.openlocfilehash: f9b9f48d671bd0cbae0b7f8a26eccb21f372c4ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591115"
---
# <span data-ttu-id="17c93-101">Get-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="17c93-101">Get-AzureRmCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="17c93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17c93-102">SYNOPSIS</span></span>
<span data-ttu-id="17c93-103">Bir hesabın API anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="17c93-103">Gets the API keys for an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17c93-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="17c93-104">SYNTAX</span></span>

```
Get-AzureRmCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17c93-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="17c93-105">DESCRIPTION</span></span>
<span data-ttu-id="17c93-106">**Get-Azurermöğretici Iveservicesaccountkey** cmdlet 'i, sağlanan bir öğretici hizmet HESABı için API anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="17c93-106">The **Get-AzureRmCognitiveServicesAccountKey** cmdlet gets the API keys for a provisioned Cognitive Services account.</span></span>

<span data-ttu-id="17c93-107">Bir öğretici Hizmetler hesabında iki API tuşu vardır: anahtar ve Anahtar2.</span><span class="sxs-lookup"><span data-stu-id="17c93-107">A Cognitive Services account has two API keys: Key1 and Key2.</span></span>
<span data-ttu-id="17c93-108">Tuşlar, öğretici hizmet hesabı uç noktasıyla etkileşimi etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="17c93-108">The keys enable interaction with the Cognitive Services account endpoint.</span></span>

<span data-ttu-id="17c93-109">Anahtarı yeniden oluşturmak için New-AzureRmCognitiveServicesAccountKey kullanın.</span><span class="sxs-lookup"><span data-stu-id="17c93-109">Use New-AzureRmCognitiveServicesAccountKey to regenerate a key.</span></span>

## <span data-ttu-id="17c93-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="17c93-110">EXAMPLES</span></span>

## <span data-ttu-id="17c93-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="17c93-111">PARAMETERS</span></span>

### <span data-ttu-id="17c93-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="17c93-112">-Name</span></span>
<span data-ttu-id="17c93-113">Hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17c93-113">Specifies the name of the account.</span></span>
<span data-ttu-id="17c93-114">Bu cmdlet bu hesabın anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="17c93-114">This cmdlet gets the keys for this account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17c93-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17c93-115">-ResourceGroupName</span></span>
<span data-ttu-id="17c93-116">Hesabın atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17c93-116">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17c93-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17c93-117">-DefaultProfile</span></span>
<span data-ttu-id="17c93-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="17c93-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17c93-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17c93-119">CommonParameters</span></span>
<span data-ttu-id="17c93-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="17c93-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17c93-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17c93-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17c93-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="17c93-122">INPUTS</span></span>

## <span data-ttu-id="17c93-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="17c93-123">OUTPUTS</span></span>

### <span data-ttu-id="17c93-124">Microsoft. Azure. Commands. Management. öğretici ınitialveservices. modeller. Psöğretici Iveservicesaccountkeys</span><span class="sxs-lookup"><span data-stu-id="17c93-124">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="17c93-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="17c93-125">NOTES</span></span>

## <span data-ttu-id="17c93-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="17c93-126">RELATED LINKS</span></span>

[<span data-ttu-id="17c93-127">New-Azurermöğretici Iveservicesaccountkey</span><span class="sxs-lookup"><span data-stu-id="17c93-127">New-AzureRmCognitiveServicesAccountKey</span></span>](./New-AzureRmCognitiveServicesAccountKey.md)


