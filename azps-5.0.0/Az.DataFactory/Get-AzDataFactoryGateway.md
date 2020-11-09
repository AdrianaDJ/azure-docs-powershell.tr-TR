---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: D85FF5ED-23EA-48C7-8E61-D931713E0064
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGateway.md
ms.openlocfilehash: 6d7b82a3046b56b473140b6830a0b04333cba9b0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321069"
---
# <span data-ttu-id="4f738-101">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="4f738-101">Get-AzDataFactoryGateway</span></span>

## <span data-ttu-id="4f738-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f738-102">SYNOPSIS</span></span>
<span data-ttu-id="4f738-103">Azure Veri Fabrikası 'ndaki mantıksal ağ geçitleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="4f738-103">Gets information about logical gateways in Azure Data Factory.</span></span>

## <span data-ttu-id="4f738-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4f738-104">SYNTAX</span></span>

### <span data-ttu-id="4f738-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4f738-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryGateway [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f738-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4f738-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f738-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4f738-107">DESCRIPTION</span></span>
<span data-ttu-id="4f738-108">**Get-AzDataFactoryGateway** cmdlet 'ı, Azure Data Factory 'deki mantıksal ağ geçitleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="4f738-108">The **Get-AzDataFactoryGateway** cmdlet gets information about logical gateways in Azure Data Factory.</span></span>
<span data-ttu-id="4f738-109">Ağ geçidinin adını belirtirseniz, bu cmdlet bu ağ geçidi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="4f738-109">If you specify the name of a gateway, this cmdlet gets information about that gateway.</span></span>
<span data-ttu-id="4f738-110">Bir ad belirtmezseniz, bu cmdlet Veri Fabrikası için tüm ağ geçitlerinde bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="4f738-110">If you do not specify a name, this cmdlet gets information about all gateways for a data factory.</span></span>
<span data-ttu-id="4f738-111">Bir şirket içi Microsoft SQL Server 'ı bir veri fabrikasına bağlı hizmet olarak eklemek istiyorsanız, şirket içi bilgisayarınıza bir ağ geçidi yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="4f738-111">If you want to add an on-premises Microsoft SQL Server as a linked service to a data factory, you must install a gateway on your on-premises computer.</span></span>

## <span data-ttu-id="4f738-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4f738-112">EXAMPLES</span></span>

### <span data-ttu-id="4f738-113">Örnek 1: Veri Fabrikası içindeki tüm mantıksal ağ geçitlerini alma</span><span class="sxs-lookup"><span data-stu-id="4f738-113">Example 1: Get all logical gateways in a data factory</span></span>
```
PS C:\>Get-AzDataFactoryGateway -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
Name            : gateway1
Description     : 
Version         : 1.3.5338.1
Status          : Online
VersionStatus   : UpToDate
CreateTime      : 8/22/2014 1:40:34 AM
RegisterTime    : 8/22/2014 1:41:46 AM
LastConnectTime : 8/22/2014 1:44:56 AM
ExpiryTime      : 
Name            : gateway2
Description     : 
Version         : 1.3.5338.1
Status          : Offline
VersionStatus   : UpToDate
CreateTime      : 8/29/2014 1:46:44 AM
RegisterTime    : 8/29/2014 1:48:36 AM
LastConnectTime : 8/29/2014 1:56:56 AM
ExpiryTime      :
```

<span data-ttu-id="4f738-114">Bu komut, ADF adlı kaynak grubundaki WikiADF adlı veri fabrikası için tüm mantıksal ağ geçitleriyle ilgili bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="4f738-114">This command gets information about all logical gateways for the data factory named WikiADF in the resource group named ADF.</span></span>

### <span data-ttu-id="4f738-115">Örnek 2: Veri Fabrikası</span><span class="sxs-lookup"><span data-stu-id="4f738-115">Example 2: Get a specific logical gateway in a data factory</span></span>
```
PS C:\>Get-AzDataFactoryGateway -ResourceGroupName "ADF" -Name "Gateway01" -DataFactoryName "WikiADF"
Name            : Gateway01
Description     : 
Version         : 1.3.5338.1
Status          : Online
VersionStatus   : UpToDate
CreateTime      : 8/22/2014 1:40:34 AM
RegisterTime    : 8/22/2014 1:41:46 AM
LastConnectTime : 8/22/2014 1:44:56 AM
ExpiryTime      :
```

<span data-ttu-id="4f738-116">Bu komut, ADF adlı kaynak grubundaki WikiADF adındaki Gateway01 adındaki mantıksal ağ geçidi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="4f738-116">This command gets information about the logical gateway named Gateway01 in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="4f738-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4f738-117">PARAMETERS</span></span>

### <span data-ttu-id="4f738-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="4f738-118">-DataFactory</span></span>
<span data-ttu-id="4f738-119">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f738-119">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="4f738-120">Bu cmdlet, bu parametrenin belirttiği veri fabrikası içindeki mantıksal ağ geçitleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="4f738-120">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4f738-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4f738-121">-DataFactoryName</span></span>
<span data-ttu-id="4f738-122">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f738-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="4f738-123">Bu cmdlet, bu parametrenin belirttiği veri fabrikası içindeki mantıksal ağ geçitleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="4f738-123">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4f738-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f738-124">-DefaultProfile</span></span>
<span data-ttu-id="4f738-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4f738-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f738-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="4f738-126">-Name</span></span>
<span data-ttu-id="4f738-127">Bilgi alınacak mantıksal ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f738-127">Specifies the name of the logical gateway about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f738-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f738-128">-ResourceGroupName</span></span>
<span data-ttu-id="4f738-129">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f738-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="4f738-130">Bu cmdlet, bu parametrenin belirttiği gruba ait mantıksal ağ geçitleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="4f738-130">This cmdlet gets information about logical gateways that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4f738-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f738-131">CommonParameters</span></span>
<span data-ttu-id="4f738-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4f738-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f738-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f738-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f738-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4f738-134">INPUTS</span></span>

### <span data-ttu-id="4f738-135">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="4f738-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="4f738-136">System. String</span><span class="sxs-lookup"><span data-stu-id="4f738-136">System.String</span></span>

## <span data-ttu-id="4f738-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4f738-137">OUTPUTS</span></span>

### <span data-ttu-id="4f738-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="4f738-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="4f738-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4f738-139">NOTES</span></span>
* <span data-ttu-id="4f738-140">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="4f738-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4f738-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4f738-141">RELATED LINKS</span></span>

[<span data-ttu-id="4f738-142">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="4f738-142">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="4f738-143">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="4f738-143">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)

[<span data-ttu-id="4f738-144">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="4f738-144">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


