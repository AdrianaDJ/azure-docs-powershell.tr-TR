---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 73B1EB7E-568E-44E8-993A-91678B7D8AEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: 8150abc726f990b699237dbaad3641a99bae2e2c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095795"
---
# <span data-ttu-id="bdbbd-101">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="bdbbd-101">Get-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="bdbbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdbbd-102">SYNOPSIS</span></span>
<span data-ttu-id="bdbbd-103">Bir hesabın API anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="bdbbd-103">Gets the API keys for an account.</span></span>

## <span data-ttu-id="bdbbd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bdbbd-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bdbbd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bdbbd-105">DESCRIPTION</span></span>
<span data-ttu-id="bdbbd-106">**Get-az, Itiveservicesaccountkey** cmdlet 'i, sağlanan bir öğretici hizmet HESABı için API anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="bdbbd-106">The **Get-AzCognitiveServicesAccountKey** cmdlet gets the API keys for a provisioned Cognitive Services account.</span></span>
<span data-ttu-id="bdbbd-107">Bir öğretici Hizmetler hesabında iki API tuşu vardır: anahtar ve Anahtar2.</span><span class="sxs-lookup"><span data-stu-id="bdbbd-107">A Cognitive Services account has two API keys: Key1 and Key2.</span></span>
<span data-ttu-id="bdbbd-108">Tuşlar, öğretici hizmet hesabı uç noktasıyla etkileşimi etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="bdbbd-108">The keys enable interaction with the Cognitive Services account endpoint.</span></span>
<span data-ttu-id="bdbbd-109">Anahtarı yeniden oluşturmak için New-AzCognitiveServicesAccountKey kullanın.</span><span class="sxs-lookup"><span data-stu-id="bdbbd-109">Use New-AzCognitiveServicesAccountKey to regenerate a key.</span></span>

## <span data-ttu-id="bdbbd-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bdbbd-110">EXAMPLES</span></span>

### <span data-ttu-id="bdbbd-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bdbbd-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="bdbbd-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bdbbd-112">PARAMETERS</span></span>

### <span data-ttu-id="bdbbd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdbbd-113">-DefaultProfile</span></span>
<span data-ttu-id="bdbbd-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="bdbbd-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bdbbd-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="bdbbd-115">-Name</span></span>
<span data-ttu-id="bdbbd-116">Hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bdbbd-116">Specifies the name of the account.</span></span>
<span data-ttu-id="bdbbd-117">Bu cmdlet bu hesabın anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="bdbbd-117">This cmdlet gets the keys for this account.</span></span>

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

### <span data-ttu-id="bdbbd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdbbd-118">-ResourceGroupName</span></span>
<span data-ttu-id="bdbbd-119">Hesabın atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bdbbd-119">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="bdbbd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdbbd-120">CommonParameters</span></span>
<span data-ttu-id="bdbbd-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bdbbd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdbbd-122">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bdbbd-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdbbd-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bdbbd-123">INPUTS</span></span>

### <span data-ttu-id="bdbbd-124">System. String</span><span class="sxs-lookup"><span data-stu-id="bdbbd-124">System.String</span></span>

## <span data-ttu-id="bdbbd-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bdbbd-125">OUTPUTS</span></span>

### <span data-ttu-id="bdbbd-126">Microsoft. Azure. Commands. Management. öğretici ınitialveservices. modeller. Psöğretici Iveservicesaccountkeys</span><span class="sxs-lookup"><span data-stu-id="bdbbd-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="bdbbd-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bdbbd-127">NOTES</span></span>

## <span data-ttu-id="bdbbd-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bdbbd-128">RELATED LINKS</span></span>

[<span data-ttu-id="bdbbd-129">New-az</span><span class="sxs-lookup"><span data-stu-id="bdbbd-129">New-AzCognitiveServicesAccountKey</span></span>](./New-AzCognitiveServicesAccountKey.md)


