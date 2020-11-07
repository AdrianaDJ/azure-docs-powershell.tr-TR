---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 663D27A3-0B51-48F5-81D0-8DDBC5A3A33C
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryGateway.md
ms.openlocfilehash: 765fbe54a43ee28e2ccce8254a6f146c734b0e03
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752459"
---
# <span data-ttu-id="fa036-101">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="fa036-101">Set-AzDataFactoryGateway</span></span>

## <span data-ttu-id="fa036-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa036-102">SYNOPSIS</span></span>
<span data-ttu-id="fa036-103">Azure Veri Fabrikası 'nde ağ geçidinin açıklamasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="fa036-103">Sets the description for a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="fa036-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fa036-104">SYNTAX</span></span>

### <span data-ttu-id="fa036-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fa036-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Description] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa036-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="fa036-106">ByFactoryObject</span></span>
```
Set-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa036-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fa036-107">DESCRIPTION</span></span>
<span data-ttu-id="fa036-108">**Set-AzDataFactoryGateway** cmdlet 'ı, Azure Veri Fabrikası 'nde belirtilen ağ geçidinin açıklamasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="fa036-108">The **Set-AzDataFactoryGateway** cmdlet sets the description for the specified gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="fa036-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fa036-109">EXAMPLES</span></span>

### <span data-ttu-id="fa036-110">Örnek 1: ağ geçidi için açıklama ayarlama</span><span class="sxs-lookup"><span data-stu-id="fa036-110">Example 1: Set the description for a gateway</span></span>
```
PS C:\>Set-AzDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
Name            : ContosoGateway
Description     : my gateway
Version         : 1.3.5338.1
Status          : Online
VersionStatus   : UpToDate
CreateTime      : 8/22/2014 1:31:09 AM
RegisterTime    : 8/22/2014 1:31:37 AM
LastConnectTime : 8/22/2014 1:41:41 AM
ExpiryTime      :
```

<span data-ttu-id="fa036-111">Bu komut, WikiADF adlı veri fabrikası</span><span class="sxs-lookup"><span data-stu-id="fa036-111">This command sets the description for the gateway named ContosoGateway in the data factory named WikiADF.</span></span>
<span data-ttu-id="fa036-112">Açıklama parametresi yeni açıklamayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa036-112">The Description parameter specifies the new description.</span></span>

## <span data-ttu-id="fa036-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fa036-113">PARAMETERS</span></span>

### <span data-ttu-id="fa036-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="fa036-114">-DataFactory</span></span>
<span data-ttu-id="fa036-115">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa036-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="fa036-116">Bu cmdlet, bu parametrenin belirttiği veri fabrikasında ağ geçidinin açıklamasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="fa036-116">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="fa036-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="fa036-117">-DataFactoryName</span></span>
<span data-ttu-id="fa036-118">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa036-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="fa036-119">Bu cmdlet, bu parametrenin belirttiği veri fabrikasında ağ geçidinin açıklamasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="fa036-119">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="fa036-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa036-120">-DefaultProfile</span></span>
<span data-ttu-id="fa036-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fa036-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa036-122">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="fa036-122">-Description</span></span>
<span data-ttu-id="fa036-123">Ağ Geçidi için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa036-123">Specifies a description for the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa036-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="fa036-124">-Name</span></span>
<span data-ttu-id="fa036-125">Açıklaması ayarlanacak ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa036-125">Specifies the name of the gateway for which to set a description.</span></span>

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

### <span data-ttu-id="fa036-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa036-126">-ResourceGroupName</span></span>
<span data-ttu-id="fa036-127">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa036-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="fa036-128">Bu cmdlet, bu parametrenin belirttiği gruba ait bir ağ geçidinin açıklamasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="fa036-128">This cmdlet sets the description for a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="fa036-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa036-129">CommonParameters</span></span>
<span data-ttu-id="fa036-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fa036-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa036-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa036-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa036-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fa036-132">INPUTS</span></span>

### <span data-ttu-id="fa036-133">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="fa036-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="fa036-134">System. String</span><span class="sxs-lookup"><span data-stu-id="fa036-134">System.String</span></span>

## <span data-ttu-id="fa036-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fa036-135">OUTPUTS</span></span>

### <span data-ttu-id="fa036-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="fa036-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="fa036-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fa036-137">NOTES</span></span>
* <span data-ttu-id="fa036-138">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="fa036-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="fa036-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fa036-139">RELATED LINKS</span></span>

[<span data-ttu-id="fa036-140">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="fa036-140">Get-AzDataFactoryGateway</span></span>](./Get-AzDataFactoryGateway.md)

[<span data-ttu-id="fa036-141">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="fa036-141">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="fa036-142">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="fa036-142">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)


