---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 8546C3FE-5396-4027-BF33-F98F6C018A67
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactorygatewaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayKey.md
ms.openlocfilehash: 1e637fdad3d6423a5d41eaf4d1dcfe682bf99fd9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764145"
---
# <span data-ttu-id="f5c5d-101">New-AzureRmDataFactoryGatewayKey</span><span class="sxs-lookup"><span data-stu-id="f5c5d-101">New-AzureRmDataFactoryGatewayKey</span></span>

## <span data-ttu-id="f5c5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5c5d-102">SYNOPSIS</span></span>
<span data-ttu-id="f5c5d-103">Bir Azure Veri Fabrikası için ağ geçidi anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f5c5d-103">Creates a gateway key for an Azure Data Factory.</span></span> <span data-ttu-id="f5c5d-104">Bu cmdlet kullanım dışıdır ve bunun yerine **New-AzureRmDataFactoryGatewayAuthKey** kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="f5c5d-104">This cmdlet is deprecated, and you should use **New-AzureRmDataFactoryGatewayAuthKey** instead.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5c5d-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f5c5d-105">SYNTAX</span></span>

### <span data-ttu-id="f5c5d-106">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f5c5d-106">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryGatewayKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5c5d-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f5c5d-107">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryGatewayKey [-DataFactory] <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5c5d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f5c5d-108">DESCRIPTION</span></span>
<span data-ttu-id="f5c5d-109">**Yeni-AzureRmDataFactoryGatewayKey** cmdlet 'i, belirli bir Azure Data Factory ağ geçidi için bir ağ geçidi anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f5c5d-109">The **New-AzureRmDataFactoryGatewayKey** cmdlet creates a gateway key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="f5c5d-110">Bu anahtarı kullanarak ağ geçidini bir bulut hizmetiyle kaydedersiniz.</span><span class="sxs-lookup"><span data-stu-id="f5c5d-110">You register the gateway with a cloud service by using this key.</span></span> <span data-ttu-id="f5c5d-111">Bu cmdlet kullanım dışıdır ve bunun yerine **New-AzureRmDataFactoryGatewayAuthKey** kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="f5c5d-111">This cmdlet is deprecated, and you should use **New-AzureRmDataFactoryGatewayAuthKey** instead.</span></span>

## <span data-ttu-id="f5c5d-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f5c5d-112">EXAMPLES</span></span>

### <span data-ttu-id="f5c5d-113">Örnek 1: ağ geçidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="f5c5d-113">Example 1: Create a gateway key</span></span>
```
PS C:\>New-AzureRmDataFactoryGatewayKey -ResourceGroupName "ADF" -GatewayName "ContosoGateway" -DataFactoryName "WikiADF" | Format-List
GatewayKey : ADF#40cbb3d9-2736-4794-a8a6-e6b839b4894f@a2d875ce-c9d7-4b8b-ad65-dd3ebbb9a940@8c0d1801-e863-44af-82e6-fb2f0c00f2ae@xz#Y9R0NhAeH3u7wgnrJyiWj4Y/QIhH4fFilIdzZgwsVQA=
```

<span data-ttu-id="f5c5d-114">Bu komut, ContosoGateway adlı Data Factory ağ geçidi için bir ağ geçidi anahtarı oluşturur ve ardından kanal işlecini kullanarak ağ geçidi anahtarını Format-List cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="f5c5d-114">This command creates a gateway key for the data factory gateway named ContosoGateway, and then passes the gateway key to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f5c5d-115">Daha fazla bilgi için yazın `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="f5c5d-115">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="f5c5d-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f5c5d-116">PARAMETERS</span></span>

### <span data-ttu-id="f5c5d-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5c5d-117">-DataFactory</span></span>
<span data-ttu-id="f5c5d-118">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5c5d-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="f5c5d-119">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bir ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f5c5d-119">This cmdlet creates a gateway key for the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5c5d-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f5c5d-120">-DataFactoryName</span></span>
<span data-ttu-id="f5c5d-121">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5c5d-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f5c5d-122">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bir ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f5c5d-122">This cmdlet creates a gateway key for the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5c5d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5c5d-123">-DefaultProfile</span></span>
<span data-ttu-id="f5c5d-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f5c5d-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5c5d-125">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="f5c5d-125">-GatewayName</span></span>
<span data-ttu-id="f5c5d-126">Ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5c5d-126">Specifies the name of the gateway.</span></span>
<span data-ttu-id="f5c5d-127">Bu cmdlet, bu parametrenin belirttiği ağ geçidi için bir anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f5c5d-127">This cmdlet creates a key for the gateway that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5c5d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5c5d-128">-ResourceGroupName</span></span>
<span data-ttu-id="f5c5d-129">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5c5d-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f5c5d-130">Bu cmdlet, bu parametrenin belirttiği gruba ait bir ağ geçidi için anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f5c5d-130">This cmdlet creates a key for a gateway that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5c5d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5c5d-131">CommonParameters</span></span>
<span data-ttu-id="f5c5d-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f5c5d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5c5d-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5c5d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5c5d-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f5c5d-134">INPUTS</span></span>

### <span data-ttu-id="f5c5d-135">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="f5c5d-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="f5c5d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f5c5d-136">System.String</span></span>

## <span data-ttu-id="f5c5d-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f5c5d-137">OUTPUTS</span></span>

### <span data-ttu-id="f5c5d-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayKey</span><span class="sxs-lookup"><span data-stu-id="f5c5d-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayKey</span></span>

## <span data-ttu-id="f5c5d-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f5c5d-139">NOTES</span></span>
* <span data-ttu-id="f5c5d-140">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="f5c5d-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f5c5d-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f5c5d-141">RELATED LINKS</span></span>

<span data-ttu-id="f5c5d-142">[Yeni-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md) 
 [Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md) 
 [Yeni-AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="f5c5d-142">[New-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md)
[Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md)
[New-AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span></span>

