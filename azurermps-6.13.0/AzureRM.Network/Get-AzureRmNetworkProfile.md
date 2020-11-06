---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkProfile.md
ms.openlocfilehash: 5bdd5e5d5212564afb1f9b06f220e8c452bcbbaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595078"
---
# <span data-ttu-id="78fde-101">Get-AzureRmNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="78fde-101">Get-AzureRmNetworkProfile</span></span>

## <span data-ttu-id="78fde-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78fde-102">SYNOPSIS</span></span>
<span data-ttu-id="78fde-103">Var olan bir ağ profili üst düzey kaynağını alır</span><span class="sxs-lookup"><span data-stu-id="78fde-103">Gets an existing network profile top level resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78fde-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="78fde-104">SYNTAX</span></span>

### <span data-ttu-id="78fde-105">NoExpand (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="78fde-105">NoExpand (Default)</span></span>
```
Get-AzureRmNetworkProfile [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78fde-106">GetByResourceNameExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="78fde-106">GetByResourceNameExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78fde-107">Getbyresourcenparameteroexpandparameterset</span><span class="sxs-lookup"><span data-stu-id="78fde-107">GetByResourceNameNoExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile [-ResourceGroupName <String>] [-Name <String>] -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78fde-108">Getbyresourceidexpanvseçparameterset</span><span class="sxs-lookup"><span data-stu-id="78fde-108">GetByResourceIdExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile -ResourceId <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78fde-109">Getbyresourceıdnoexpandparameterset</span><span class="sxs-lookup"><span data-stu-id="78fde-109">GetByResourceIdNoExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile -ResourceId <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78fde-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="78fde-110">DESCRIPTION</span></span>
<span data-ttu-id="78fde-111">**Get-AzureRmNetworkProfile** cmdlet 'i mevcut bir ağ profili üst düzey kaynağı alır</span><span class="sxs-lookup"><span data-stu-id="78fde-111">The **Get-AzureRmNetworkProfile** cmdlet retrieves an existing network profile top level resource</span></span>

## <span data-ttu-id="78fde-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="78fde-112">EXAMPLES</span></span>

### <span data-ttu-id="78fde-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="78fde-113">Example 1</span></span>
```powershell
$networkProfile = Get-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="78fde-114">Bu, kaynak grubundaki NP1 ağ profilini alır RG1</span><span class="sxs-lookup"><span data-stu-id="78fde-114">This retrieves the network profile np1 in resource group rg1</span></span>

## <span data-ttu-id="78fde-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="78fde-115">PARAMETERS</span></span>

### <span data-ttu-id="78fde-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78fde-116">-DefaultProfile</span></span>
<span data-ttu-id="78fde-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="78fde-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78fde-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="78fde-118">-ExpandResource</span></span>
<span data-ttu-id="78fde-119">Genişletilecek kaynak başvurusu.</span><span class="sxs-lookup"><span data-stu-id="78fde-119">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet, GetByResourceNameNoExpandParameterSet, GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78fde-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="78fde-120">-Name</span></span>
<span data-ttu-id="78fde-121">Ağ profilinin adı.</span><span class="sxs-lookup"><span data-stu-id="78fde-121">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78fde-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78fde-122">-ResourceGroupName</span></span>
<span data-ttu-id="78fde-123">Ağ profilinin kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="78fde-123">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78fde-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="78fde-124">-ResourceId</span></span>
<span data-ttu-id="78fde-125">Ağ profilinin Azure Kaynak Yöneticisi kimliği.</span><span class="sxs-lookup"><span data-stu-id="78fde-125">The Azure resource manager id of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78fde-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78fde-126">CommonParameters</span></span>
<span data-ttu-id="78fde-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="78fde-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78fde-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78fde-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78fde-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="78fde-129">INPUTS</span></span>

### <span data-ttu-id="78fde-130">System. String</span><span class="sxs-lookup"><span data-stu-id="78fde-130">System.String</span></span>

## <span data-ttu-id="78fde-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="78fde-131">OUTPUTS</span></span>

### <span data-ttu-id="78fde-132">Microsoft. Azure. Commands. Network. modeller. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="78fde-132">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="78fde-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="78fde-133">NOTES</span></span>

## <span data-ttu-id="78fde-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="78fde-134">RELATED LINKS</span></span>
