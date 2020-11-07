---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGatewayAuthKey.md
ms.openlocfilehash: 9e677417ed1d592da04d8023a7cc58826662fada
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762739"
---
# <span data-ttu-id="5ebd7-101">Get-AzureRmDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="5ebd7-101">Get-AzureRmDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="5ebd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ebd7-102">SYNOPSIS</span></span>
<span data-ttu-id="5ebd7-103">Bir Azure Veri Fabrikası için ağ geçidi doğrulama anahtarını alır.</span><span class="sxs-lookup"><span data-stu-id="5ebd7-103">Gets gateway auth key for an Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ebd7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5ebd7-104">SYNTAX</span></span>

### <span data-ttu-id="5ebd7-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5ebd7-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ebd7-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="5ebd7-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ebd7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5ebd7-107">DESCRIPTION</span></span>
<span data-ttu-id="5ebd7-108">**Get-AzureRmDataFactoryGatewayAuthKey** cmdlet 'i, belirli bir Azure Data Factory ağ geçidi için ağ geçidi doğrulama anahtarını alır.</span><span class="sxs-lookup"><span data-stu-id="5ebd7-108">The **Get-AzureRmDataFactoryGatewayAuthKey** cmdlet gets gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="5ebd7-109">Bu kimlik doğrulama anahtarının bu anahtar veya anahtar2 kullanarak ağ geçidini bir bulut hizmetiyle kaydedersiniz.</span><span class="sxs-lookup"><span data-stu-id="5ebd7-109">You register the gateway with a cloud service by using this key1 or key2 of this auth key.</span></span>

## <span data-ttu-id="5ebd7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5ebd7-110">EXAMPLES</span></span>

### <span data-ttu-id="5ebd7-111">Örnek 1: bir ağ geçidinin auth anahtarını alır</span><span class="sxs-lookup"><span data-stu-id="5ebd7-111">Example 1: Gets auth key of a gateway</span></span>
```
PS C:\> Get-AzureRmDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@ZgBjjX6GfJcrzTQInEV9PoOqsDrqOmC
       gGHqUg1THLqA=
Key2 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@kFXxBdFCEBeL7LPB3hA3LqLd1uNFbyv
       YmWxtV4WD3JQ=
```

<span data-ttu-id="5ebd7-112">Bu komut MyGateway adlı Data Factory ağ geçidi için geçit kimlik doğrulama anahtarını alır.</span><span class="sxs-lookup"><span data-stu-id="5ebd7-112">This command gets gateway auth key for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="5ebd7-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5ebd7-113">PARAMETERS</span></span>

### <span data-ttu-id="5ebd7-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5ebd7-114">-DataFactoryName</span></span>
<span data-ttu-id="5ebd7-115">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="5ebd7-115">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ebd7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ebd7-116">-DefaultProfile</span></span>
<span data-ttu-id="5ebd7-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5ebd7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ebd7-118">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="5ebd7-118">-GatewayName</span></span>
<span data-ttu-id="5ebd7-119">Veri Fabrikası ağ geçidi adı.</span><span class="sxs-lookup"><span data-stu-id="5ebd7-119">The data factory gateway name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ebd7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ebd7-120">-InputObject</span></span>
<span data-ttu-id="5ebd7-121">Veri fabrikası nesnesi</span><span class="sxs-lookup"><span data-stu-id="5ebd7-121">The data factory object</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: DataFactory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ebd7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ebd7-122">-ResourceGroupName</span></span>
<span data-ttu-id="5ebd7-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="5ebd7-123">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ebd7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ebd7-124">CommonParameters</span></span>
<span data-ttu-id="5ebd7-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5ebd7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ebd7-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ebd7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ebd7-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5ebd7-127">INPUTS</span></span>

### <span data-ttu-id="5ebd7-128">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="5ebd7-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>
<span data-ttu-id="5ebd7-129">System. String</span><span class="sxs-lookup"><span data-stu-id="5ebd7-129">System.String</span></span>

## <span data-ttu-id="5ebd7-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5ebd7-130">OUTPUTS</span></span>

### <span data-ttu-id="5ebd7-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="5ebd7-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="5ebd7-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5ebd7-132">NOTES</span></span>
* <span data-ttu-id="5ebd7-133">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="5ebd7-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5ebd7-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5ebd7-134">RELATED LINKS</span></span>

<span data-ttu-id="5ebd7-135">[Yeni-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md) 
 [Yeni-AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="5ebd7-135">[New-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md)
[New-AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span></span>

