---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 663D27A3-0B51-48F5-81D0-8DDBC5A3A33C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryGateway.md
ms.openlocfilehash: 2cca641538be35f18173fd1e03b5f593c87649bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588248"
---
# <span data-ttu-id="e4906-101">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="e4906-101">Set-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="e4906-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4906-102">SYNOPSIS</span></span>
<span data-ttu-id="e4906-103">Azure Veri Fabrikası 'nde ağ geçidinin açıklamasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e4906-103">Sets the description for a gateway in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4906-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e4906-104">SYNTAX</span></span>

### <span data-ttu-id="e4906-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e4906-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Description] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4906-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e4906-106">ByFactoryObject</span></span>
```
Set-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4906-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e4906-107">DESCRIPTION</span></span>
<span data-ttu-id="e4906-108">**Set-AzureRmDataFactoryGateway** cmdlet 'ı, Azure Veri Fabrikası 'nde belirtilen ağ geçidinin açıklamasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e4906-108">The **Set-AzureRmDataFactoryGateway** cmdlet sets the description for the specified gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="e4906-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e4906-109">EXAMPLES</span></span>

### <span data-ttu-id="e4906-110">Örnek 1: ağ geçidi için açıklama ayarlama</span><span class="sxs-lookup"><span data-stu-id="e4906-110">Example 1: Set the description for a gateway</span></span>
```
PS C:\>Set-AzureRmDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
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

<span data-ttu-id="e4906-111">Bu komut, WikiADF adlı veri fabrikası</span><span class="sxs-lookup"><span data-stu-id="e4906-111">This command sets the description for the gateway named ContosoGateway in the data factory named WikiADF.</span></span>
<span data-ttu-id="e4906-112">Açıklama parametresi yeni açıklamayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4906-112">The Description parameter specifies the new description.</span></span>

## <span data-ttu-id="e4906-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e4906-113">PARAMETERS</span></span>

### <span data-ttu-id="e4906-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="e4906-114">-DataFactory</span></span>
<span data-ttu-id="e4906-115">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4906-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="e4906-116">Bu cmdlet, bu parametrenin belirttiği veri fabrikasında ağ geçidinin açıklamasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e4906-116">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e4906-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e4906-117">-DataFactoryName</span></span>
<span data-ttu-id="e4906-118">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4906-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="e4906-119">Bu cmdlet, bu parametrenin belirttiği veri fabrikasında ağ geçidinin açıklamasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e4906-119">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e4906-120">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="e4906-120">-Description</span></span>
<span data-ttu-id="e4906-121">Ağ Geçidi için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4906-121">Specifies a description for the gateway.</span></span>

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

### <span data-ttu-id="e4906-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="e4906-122">-Name</span></span>
<span data-ttu-id="e4906-123">Açıklaması ayarlanacak ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4906-123">Specifies the name of the gateway for which to set a description.</span></span>

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

### <span data-ttu-id="e4906-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4906-124">-ResourceGroupName</span></span>
<span data-ttu-id="e4906-125">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4906-125">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e4906-126">Bu cmdlet, bu parametrenin belirttiği gruba ait bir ağ geçidinin açıklamasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e4906-126">This cmdlet sets the description for a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e4906-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4906-127">-DefaultProfile</span></span>
<span data-ttu-id="e4906-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e4906-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4906-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4906-129">CommonParameters</span></span>
<span data-ttu-id="e4906-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e4906-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4906-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4906-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4906-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e4906-132">INPUTS</span></span>

## <span data-ttu-id="e4906-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e4906-133">OUTPUTS</span></span>

### <span data-ttu-id="e4906-134">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway]], Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="e4906-134">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway]], Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway</span></span>

## <span data-ttu-id="e4906-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e4906-135">NOTES</span></span>
* <span data-ttu-id="e4906-136">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="e4906-136">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e4906-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e4906-137">RELATED LINKS</span></span>

[<span data-ttu-id="e4906-138">Get-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="e4906-138">Get-AzureRmDataFactoryGateway</span></span>](./Get-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="e4906-139">Yeni-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="e4906-139">New-AzureRmDataFactoryGateway</span></span>](./New-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="e4906-140">Remove-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="e4906-140">Remove-AzureRmDataFactoryGateway</span></span>](./Remove-AzureRmDataFactoryGateway.md)


