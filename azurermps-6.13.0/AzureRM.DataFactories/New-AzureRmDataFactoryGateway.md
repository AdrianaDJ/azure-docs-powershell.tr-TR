---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 4DCF54BA-CFFA-4555-8CA3-66B98F704EFB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGateway.md
ms.openlocfilehash: 6e6f444b76b258be576e13efa2f036329bf0fafd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593697"
---
# <span data-ttu-id="7c23b-101">New-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="7c23b-101">New-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="7c23b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c23b-102">SYNOPSIS</span></span>
<span data-ttu-id="7c23b-103">Bir Azure Veri Fabrikası için ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7c23b-103">Creates a gateway for an Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c23b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7c23b-104">SYNTAX</span></span>

### <span data-ttu-id="7c23b-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7c23b-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [[-Description] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c23b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="7c23b-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [[-Description] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c23b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7c23b-107">DESCRIPTION</span></span>
<span data-ttu-id="7c23b-108">**Yeni-AzureRmDataFactoryGateway** cmdlet 'ı Azure Veri Fabrikası 'nde bir ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7c23b-108">The **New-AzureRmDataFactoryGateway** cmdlet creates a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="7c23b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7c23b-109">EXAMPLES</span></span>

### <span data-ttu-id="7c23b-110">Örnek 1: ağ geçidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="7c23b-110">Example 1: Create a gateway</span></span>
```
PS C:\>New-AzureRmDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
Name              : ContosoGateway
Description       : my gateway
Version           : 
Status            : NeedRegistration
VersionStatus     : None
CreateTime        : 8/22/2014 1:40:34 AM
RegisterTime      : 
LastConnectTime   : 
ExpiryTime        : 
ProvisioningState : Succeeded
Key               : ADF#40cbb3d9-2736-4794-a8a6-e6b839b4894f@a2d875ce-c9d7-4b8b-ad65-dd3ebbb9a940@8c0d1801-e863-44af-82e6-fb2f0c00f2ae@xz#Y9R0NhAeH3u7wgnrJyiWj4Y/QIhH4fFilIdzZgwsVQA=
```

<span data-ttu-id="7c23b-111">Bu komut, ADF adlı kaynak grubundaki WikiADF adlı Data Factory adlı bir ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7c23b-111">This command creates a gateway named ContosoGateway in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="7c23b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7c23b-112">PARAMETERS</span></span>

### <span data-ttu-id="7c23b-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="7c23b-113">-DataFactory</span></span>
<span data-ttu-id="7c23b-114">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7c23b-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="7c23b-115">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bir ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7c23b-115">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="7c23b-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7c23b-116">-DataFactoryName</span></span>
<span data-ttu-id="7c23b-117">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7c23b-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="7c23b-118">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bir ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7c23b-118">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="7c23b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c23b-119">-DefaultProfile</span></span>
<span data-ttu-id="7c23b-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7c23b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c23b-121">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="7c23b-121">-Description</span></span>
<span data-ttu-id="7c23b-122">Ağ Geçidi için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="7c23b-122">Specifies a description for the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c23b-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="7c23b-123">-Name</span></span>
<span data-ttu-id="7c23b-124">Oluşturulacak ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7c23b-124">Specifies the name of the gateway to create.</span></span>

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

### <span data-ttu-id="7c23b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c23b-125">-ResourceGroupName</span></span>
<span data-ttu-id="7c23b-126">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7c23b-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="7c23b-127">Bu cmdlet, bu parametrenin belirttiği gruba ait bir ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7c23b-127">This cmdlet creates a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7c23b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c23b-128">CommonParameters</span></span>
<span data-ttu-id="7c23b-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7c23b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c23b-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c23b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c23b-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7c23b-131">INPUTS</span></span>

### <span data-ttu-id="7c23b-132">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="7c23b-132">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="7c23b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="7c23b-133">System.String</span></span>

## <span data-ttu-id="7c23b-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7c23b-134">OUTPUTS</span></span>

### <span data-ttu-id="7c23b-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="7c23b-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="7c23b-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7c23b-136">NOTES</span></span>
* <span data-ttu-id="7c23b-137">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="7c23b-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="7c23b-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7c23b-138">RELATED LINKS</span></span>

[<span data-ttu-id="7c23b-139">Remove-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="7c23b-139">Remove-AzureRmDataFactoryGateway</span></span>](./Remove-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="7c23b-140">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="7c23b-140">Set-AzureRmDataFactoryGateway</span></span>](./Set-AzureRmDataFactoryGateway.md)


