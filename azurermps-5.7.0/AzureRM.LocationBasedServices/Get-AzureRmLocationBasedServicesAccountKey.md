---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/get-azurermlocationbasedservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccountKey.md
ms.openlocfilehash: 1f528bb0a80f039b9a2be7cb4cb6e4c7fbc740c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594470"
---
# <span data-ttu-id="4cca1-101">Get-AzureRmLocationBasedServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="4cca1-101">Get-AzureRmLocationBasedServicesAccountKey</span></span>

## <span data-ttu-id="4cca1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cca1-102">SYNOPSIS</span></span>
<span data-ttu-id="4cca1-103">Bir hesabın API anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="4cca1-103">Gets the API keys for an account.</span></span> <span data-ttu-id="4cca1-104">Bu tuşlar, Azure konum tabanlı hizmetler için sonraki çağrılarda kullanılan kimlik doğrulama mekanizmasıdır.</span><span class="sxs-lookup"><span data-stu-id="4cca1-104">These keys are the authentication mechanism used in subsequent calls to Azure Location Based Services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cca1-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4cca1-105">SYNTAX</span></span>

### <span data-ttu-id="4cca1-106">NameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4cca1-106">NameParameterSet (Default)</span></span>
```
Get-AzureRmLocationBasedServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cca1-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="4cca1-107">InputObjectParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccountKey [-InputObject <PSLocationBasedServicesAccount>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cca1-108">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="4cca1-108">ResourceIdParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4cca1-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="4cca1-109">DESCRIPTION</span></span>
<span data-ttu-id="4cca1-110">**Get-Azurermlocationbasevseçservicesaccountkey** cmdlet 'i, sağlanan konum tabanlı HIZMETLER hesabının API anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="4cca1-110">The **Get-AzureRmLocationBasedServicesAccountKey** cmdlet gets the API keys for a provisioned Location Based Services account.</span></span>

<span data-ttu-id="4cca1-111">Konum tabanlı hizmetler hesabında iki API tuşu vardır: birincil ve Ikincil.</span><span class="sxs-lookup"><span data-stu-id="4cca1-111">A Location Based Services account has two API keys: Primary and Secondary.</span></span>
<span data-ttu-id="4cca1-112">Tuşlar, konum tabanlı hizmetler hesabı uç noktasıyla etkileşimi etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="4cca1-112">The keys enable interaction with the Location Based Services account endpoint.</span></span>

<span data-ttu-id="4cca1-113">Bir anahtarı yeniden oluşturmak için [New-Azurermlocationbasevseçservicesaccountkey](New-AzureRmLocationBasedServicesAccountKey.md) 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="4cca1-113">Use [New-AzureRmLocationBasedServicesAccountKey](New-AzureRmLocationBasedServicesAccountKey.md) to regenerate a key.</span></span>

## <span data-ttu-id="4cca1-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4cca1-114">EXAMPLES</span></span>

### <span data-ttu-id="4cca1-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4cca1-115">Example 1</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="4cca1-116">MyResourceGroup kaynak grubundaki MyAccount adlı hesabın anahtarlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="4cca1-116">Returns the keys for the account named MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="4cca1-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="4cca1-117">Example 2</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="4cca1-118">Belirtilen konum tabanlı hizmetler hesabının anahtarlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="4cca1-118">Returns the keys for the specified Location Based Services Account.</span></span>

## <span data-ttu-id="4cca1-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4cca1-119">PARAMETERS</span></span>

### <span data-ttu-id="4cca1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cca1-120">-DefaultProfile</span></span>
<span data-ttu-id="4cca1-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4cca1-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cca1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4cca1-122">-InputObject</span></span>
<span data-ttu-id="4cca1-123">[Get-Azurermlocationbasevseçservicesaccount](Get-AzureRmLocationBasedServicesAccount.md)'dan yöneltilen konum tabanlı hizmetler hesabı.</span><span class="sxs-lookup"><span data-stu-id="4cca1-123">Location Based Services Account piped from [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span></span>

```yaml
Type: PSLocationBasedServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4cca1-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="4cca1-124">-Name</span></span>
<span data-ttu-id="4cca1-125">Konum tabanlı hizmetler hesap adı.</span><span class="sxs-lookup"><span data-stu-id="4cca1-125">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cca1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cca1-126">-ResourceGroupName</span></span>
<span data-ttu-id="4cca1-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4cca1-127">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cca1-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4cca1-128">-ResourceId</span></span>
<span data-ttu-id="4cca1-129">Konum temelli hizmetler hesabı RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="4cca1-129">Location Based Services Account ResourceId.</span></span>
```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cca1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cca1-130">CommonParameters</span></span>
<span data-ttu-id="4cca1-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4cca1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cca1-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cca1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cca1-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4cca1-133">INPUTS</span></span>

### <span data-ttu-id="4cca1-134">System. String</span><span class="sxs-lookup"><span data-stu-id="4cca1-134">System.String</span></span>

## <span data-ttu-id="4cca1-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4cca1-135">OUTPUTS</span></span>

### <span data-ttu-id="4cca1-136">Microsoft. Azure. Commands. Locationbasevseçservices. model. Pslocationbasevseçservicesaccountkeys</span><span class="sxs-lookup"><span data-stu-id="4cca1-136">Microsoft.Azure.Commands.LocationBasedServices.Models.PSLocationBasedServicesAccountKeys</span></span>

### <span data-ttu-id="4cca1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cca1-137">CommonParameters</span></span>
<span data-ttu-id="4cca1-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4cca1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cca1-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cca1-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cca1-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4cca1-140">NOTES</span></span>

## <span data-ttu-id="4cca1-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4cca1-141">RELATED LINKS</span></span>
