---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 73B1EB7E-568E-44E8-993A-91678B7D8AEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountKey.md
ms.openlocfilehash: b0e47d95d8ede448b37ef62e0b9deb7283d293c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587269"
---
# <span data-ttu-id="df785-101">Get-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="df785-101">Get-AzureRmCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="df785-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df785-102">SYNOPSIS</span></span>
<span data-ttu-id="df785-103">Bir hesabın API anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="df785-103">Gets the API keys for an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df785-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="df785-104">SYNTAX</span></span>

```
Get-AzureRmCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df785-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="df785-105">DESCRIPTION</span></span>
<span data-ttu-id="df785-106">**Get-Azurermöğretici Iveservicesaccountkey** cmdlet 'i, sağlanan bir öğretici hizmet HESABı için API anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="df785-106">The **Get-AzureRmCognitiveServicesAccountKey** cmdlet gets the API keys for a provisioned Cognitive Services account.</span></span>
<span data-ttu-id="df785-107">Bir öğretici Hizmetler hesabında iki API tuşu vardır: anahtar ve Anahtar2.</span><span class="sxs-lookup"><span data-stu-id="df785-107">A Cognitive Services account has two API keys: Key1 and Key2.</span></span>
<span data-ttu-id="df785-108">Tuşlar, öğretici hizmet hesabı uç noktasıyla etkileşimi etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="df785-108">The keys enable interaction with the Cognitive Services account endpoint.</span></span>
<span data-ttu-id="df785-109">Anahtarı yeniden oluşturmak için New-AzureRmCognitiveServicesAccountKey kullanın.</span><span class="sxs-lookup"><span data-stu-id="df785-109">Use New-AzureRmCognitiveServicesAccountKey to regenerate a key.</span></span>

## <span data-ttu-id="df785-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="df785-110">EXAMPLES</span></span>

### <span data-ttu-id="df785-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="df785-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="df785-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="df785-112">PARAMETERS</span></span>

### <span data-ttu-id="df785-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df785-113">-DefaultProfile</span></span>
<span data-ttu-id="df785-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="df785-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df785-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="df785-115">-Name</span></span>
<span data-ttu-id="df785-116">Hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="df785-116">Specifies the name of the account.</span></span>
<span data-ttu-id="df785-117">Bu cmdlet bu hesabın anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="df785-117">This cmdlet gets the keys for this account.</span></span>

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

### <span data-ttu-id="df785-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df785-118">-ResourceGroupName</span></span>
<span data-ttu-id="df785-119">Hesabın atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="df785-119">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="df785-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df785-120">CommonParameters</span></span>
<span data-ttu-id="df785-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="df785-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df785-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df785-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df785-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="df785-123">INPUTS</span></span>

### <span data-ttu-id="df785-124">System. String</span><span class="sxs-lookup"><span data-stu-id="df785-124">System.String</span></span>

## <span data-ttu-id="df785-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="df785-125">OUTPUTS</span></span>

### <span data-ttu-id="df785-126">Microsoft. Azure. Commands. Management. öğretici ınitialveservices. modeller. Psöğretici Iveservicesaccountkeys</span><span class="sxs-lookup"><span data-stu-id="df785-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="df785-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="df785-127">NOTES</span></span>

## <span data-ttu-id="df785-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="df785-128">RELATED LINKS</span></span>

[<span data-ttu-id="df785-129">New-Azurermöğretici Iveservicesaccountkey</span><span class="sxs-lookup"><span data-stu-id="df785-129">New-AzureRmCognitiveServicesAccountKey</span></span>](./New-AzureRmCognitiveServicesAccountKey.md)


