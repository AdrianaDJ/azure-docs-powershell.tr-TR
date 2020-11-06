---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 8546C3FE-5396-4027-BF33-F98F6C018A67
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayKey.md
ms.openlocfilehash: f1676d385b23711e71fbec5fb5d9131add4daaf4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590749"
---
# <span data-ttu-id="47af3-101">New-AzureRmDataFactoryGatewayKey</span><span class="sxs-lookup"><span data-stu-id="47af3-101">New-AzureRmDataFactoryGatewayKey</span></span>

## <span data-ttu-id="47af3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47af3-102">SYNOPSIS</span></span>
<span data-ttu-id="47af3-103">Bir Azure Veri Fabrikası için ağ geçidi anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="47af3-103">Creates a gateway key for an Azure Data Factory.</span></span> <span data-ttu-id="47af3-104">Bu cmdlet kullanım dışıdır ve bunun yerine **New-AzureRmDataFactoryGatewayAuthKey** kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="47af3-104">This cmdlet is deprecated, and you should use **New-AzureRmDataFactoryGatewayAuthKey** instead.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47af3-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="47af3-105">SYNTAX</span></span>

### <span data-ttu-id="47af3-106">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="47af3-106">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryGatewayKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47af3-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="47af3-107">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryGatewayKey [-DataFactory] <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47af3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="47af3-108">DESCRIPTION</span></span>
<span data-ttu-id="47af3-109">**Yeni-AzureRmDataFactoryGatewayKey** cmdlet 'i, belirli bir Azure Data Factory ağ geçidi için bir ağ geçidi anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="47af3-109">The **New-AzureRmDataFactoryGatewayKey** cmdlet creates a gateway key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="47af3-110">Bu anahtarı kullanarak ağ geçidini bir bulut hizmetiyle kaydedersiniz.</span><span class="sxs-lookup"><span data-stu-id="47af3-110">You register the gateway with a cloud service by using this key.</span></span> <span data-ttu-id="47af3-111">Bu cmdlet kullanım dışıdır ve bunun yerine **New-AzureRmDataFactoryGatewayAuthKey** kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="47af3-111">This cmdlet is deprecated, and you should use **New-AzureRmDataFactoryGatewayAuthKey** instead.</span></span>

## <span data-ttu-id="47af3-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="47af3-112">EXAMPLES</span></span>

### <span data-ttu-id="47af3-113">Örnek 1: ağ geçidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="47af3-113">Example 1: Create a gateway key</span></span>
```
PS C:\>New-AzureRmDataFactoryGatewayKey -ResourceGroupName "ADF" -GatewayName "ContosoGateway" -DataFactoryName "WikiADF" | Format-List
GatewayKey : ADF#40cbb3d9-2736-4794-a8a6-e6b839b4894f@a2d875ce-c9d7-4b8b-ad65-dd3ebbb9a940@8c0d1801-e863-44af-82e6-fb2f0c00f2ae@xz#Y9R0NhAeH3u7wgnrJyiWj4Y/QIhH4fFilIdzZgwsVQA=
```

<span data-ttu-id="47af3-114">Bu komut, ContosoGateway adlı Data Factory ağ geçidi için bir ağ geçidi anahtarı oluşturur ve ardından kanal işlecini kullanarak ağ geçidi anahtarını Format-List cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="47af3-114">This command creates a gateway key for the data factory gateway named ContosoGateway, and then passes the gateway key to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="47af3-115">Daha fazla bilgi için yazın `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="47af3-115">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="47af3-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="47af3-116">PARAMETERS</span></span>

### <span data-ttu-id="47af3-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="47af3-117">-DataFactory</span></span>
<span data-ttu-id="47af3-118">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="47af3-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="47af3-119">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bir ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="47af3-119">This cmdlet creates a gateway key for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="47af3-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="47af3-120">-DataFactoryName</span></span>
<span data-ttu-id="47af3-121">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="47af3-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="47af3-122">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bir ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="47af3-122">This cmdlet creates a gateway key for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="47af3-123">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="47af3-123">-GatewayName</span></span>
<span data-ttu-id="47af3-124">Ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="47af3-124">Specifies the name of the gateway.</span></span>
<span data-ttu-id="47af3-125">Bu cmdlet, bu parametrenin belirttiği ağ geçidi için bir anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="47af3-125">This cmdlet creates a key for the gateway that this parameter specifies.</span></span>

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

### <span data-ttu-id="47af3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47af3-126">-ResourceGroupName</span></span>
<span data-ttu-id="47af3-127">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="47af3-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="47af3-128">Bu cmdlet, bu parametrenin belirttiği gruba ait bir ağ geçidi için anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="47af3-128">This cmdlet creates a key for a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="47af3-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47af3-129">-DefaultProfile</span></span>
<span data-ttu-id="47af3-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="47af3-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47af3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47af3-131">CommonParameters</span></span>
<span data-ttu-id="47af3-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="47af3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47af3-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47af3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47af3-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="47af3-134">INPUTS</span></span>

## <span data-ttu-id="47af3-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="47af3-135">OUTPUTS</span></span>

### <span data-ttu-id="47af3-136">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGatewayKey</span><span class="sxs-lookup"><span data-stu-id="47af3-136">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGatewayKey</span></span>

## <span data-ttu-id="47af3-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="47af3-137">NOTES</span></span>
* <span data-ttu-id="47af3-138">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="47af3-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="47af3-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="47af3-139">RELATED LINKS</span></span>

<span data-ttu-id="47af3-140">[Yeni-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md) 
 [Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md) 
 [Yeni-AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="47af3-140">[New-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md)
[Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md)
[New-AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span></span>


