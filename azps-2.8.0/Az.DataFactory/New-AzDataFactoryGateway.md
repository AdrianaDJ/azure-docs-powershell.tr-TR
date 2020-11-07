---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 4DCF54BA-CFFA-4555-8CA3-66B98F704EFB
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGateway.md
ms.openlocfilehash: 80d981f4b727d713a5cdc235e9e8ea93d652a358
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752504"
---
# <span data-ttu-id="9f3cc-101">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9f3cc-101">New-AzDataFactoryGateway</span></span>

## <span data-ttu-id="9f3cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f3cc-102">SYNOPSIS</span></span>
<span data-ttu-id="9f3cc-103">Bir Azure Veri Fabrikası için ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9f3cc-103">Creates a gateway for an Azure Data Factory.</span></span>

## <span data-ttu-id="9f3cc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9f3cc-104">SYNTAX</span></span>

### <span data-ttu-id="9f3cc-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9f3cc-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [[-Description] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f3cc-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9f3cc-106">ByFactoryObject</span></span>
```
New-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [[-Description] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f3cc-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9f3cc-107">DESCRIPTION</span></span>
<span data-ttu-id="9f3cc-108">**New-AzDataFactoryGateway** cmdlet 'ı Azure Veri Fabrikası 'nde bir ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9f3cc-108">The **New-AzDataFactoryGateway** cmdlet creates a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="9f3cc-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9f3cc-109">EXAMPLES</span></span>

### <span data-ttu-id="9f3cc-110">Örnek 1: ağ geçidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="9f3cc-110">Example 1: Create a gateway</span></span>
```
PS C:\>New-AzDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
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

<span data-ttu-id="9f3cc-111">Bu komut, ADF adlı kaynak grubundaki WikiADF adlı Data Factory adlı bir ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9f3cc-111">This command creates a gateway named ContosoGateway in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="9f3cc-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9f3cc-112">PARAMETERS</span></span>

### <span data-ttu-id="9f3cc-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="9f3cc-113">-DataFactory</span></span>
<span data-ttu-id="9f3cc-114">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f3cc-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="9f3cc-115">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bir ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9f3cc-115">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9f3cc-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9f3cc-116">-DataFactoryName</span></span>
<span data-ttu-id="9f3cc-117">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f3cc-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="9f3cc-118">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bir ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9f3cc-118">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9f3cc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f3cc-119">-DefaultProfile</span></span>
<span data-ttu-id="9f3cc-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9f3cc-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f3cc-121">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="9f3cc-121">-Description</span></span>
<span data-ttu-id="9f3cc-122">Ağ Geçidi için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f3cc-122">Specifies a description for the gateway.</span></span>

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

### <span data-ttu-id="9f3cc-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="9f3cc-123">-Name</span></span>
<span data-ttu-id="9f3cc-124">Oluşturulacak ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f3cc-124">Specifies the name of the gateway to create.</span></span>

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

### <span data-ttu-id="9f3cc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f3cc-125">-ResourceGroupName</span></span>
<span data-ttu-id="9f3cc-126">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f3cc-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="9f3cc-127">Bu cmdlet, bu parametrenin belirttiği gruba ait bir ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9f3cc-127">This cmdlet creates a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9f3cc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f3cc-128">CommonParameters</span></span>
<span data-ttu-id="9f3cc-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9f3cc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f3cc-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f3cc-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f3cc-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9f3cc-131">INPUTS</span></span>

### <span data-ttu-id="9f3cc-132">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="9f3cc-132">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="9f3cc-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9f3cc-133">System.String</span></span>

## <span data-ttu-id="9f3cc-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9f3cc-134">OUTPUTS</span></span>

### <span data-ttu-id="9f3cc-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9f3cc-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="9f3cc-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9f3cc-136">NOTES</span></span>
* <span data-ttu-id="9f3cc-137">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="9f3cc-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="9f3cc-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9f3cc-138">RELATED LINKS</span></span>

[<span data-ttu-id="9f3cc-139">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9f3cc-139">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)

[<span data-ttu-id="9f3cc-140">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9f3cc-140">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)

