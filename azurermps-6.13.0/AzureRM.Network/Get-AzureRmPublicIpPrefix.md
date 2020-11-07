---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpPrefix.md
ms.openlocfilehash: 772f0a3bb1198bf5c8d00ad8c0dd708c37c92366
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762472"
---
# <span data-ttu-id="11278-101">Get-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="11278-101">Get-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="11278-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11278-102">SYNOPSIS</span></span>
<span data-ttu-id="11278-103">Genel bir IP öneki alır</span><span class="sxs-lookup"><span data-stu-id="11278-103">Gets a public IP prefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11278-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="11278-104">SYNTAX</span></span>

### <span data-ttu-id="11278-105">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="11278-105">(Default)</span></span>
```
Get-AzureRmPublicIpPrefix [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11278-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="11278-106">GetByNameParameterSet</span></span>
```
Get-AzureRmPublicIpPrefix [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11278-107">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="11278-107">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmPublicIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11278-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="11278-108">DESCRIPTION</span></span>
<span data-ttu-id="11278-109">**Get-AzureRmPublicIpPrefix** cmdlet 'i kaynak grubunda bir veya birden çok ortak IP önekini alır.</span><span class="sxs-lookup"><span data-stu-id="11278-109">The **Get-AzureRmPublicIpPrefix** cmdlet gets one or more public IP prefixes in a resource group.</span></span>

## <span data-ttu-id="11278-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="11278-110">EXAMPLES</span></span>

### <span data-ttu-id="11278-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="11278-111">Example 1</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzureRmPublicIpPrefix -ResourceGroupName $rgname -Name $prefixName
```

<span data-ttu-id="11278-112">Bu komut, kaynak grubunda $prefixName içeren genel bir IP önek kaynağı alır $rgName</span><span class="sxs-lookup"><span data-stu-id="11278-112">This command gets a public IP prefix resource with $prefixName in resource group $rgName</span></span>

## <span data-ttu-id="11278-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="11278-113">PARAMETERS</span></span>

### <span data-ttu-id="11278-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11278-114">-DefaultProfile</span></span>
<span data-ttu-id="11278-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="11278-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11278-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="11278-116">-Name</span></span>
<span data-ttu-id="11278-117">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="11278-117">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11278-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11278-118">-ResourceGroupName</span></span>
<span data-ttu-id="11278-119">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="11278-119">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11278-120">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="11278-120">-ResourceId</span></span>
<span data-ttu-id="11278-121">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="11278-121">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11278-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11278-122">CommonParameters</span></span>
<span data-ttu-id="11278-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="11278-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="11278-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11278-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11278-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="11278-125">INPUTS</span></span>

### <span data-ttu-id="11278-126">System. String</span><span class="sxs-lookup"><span data-stu-id="11278-126">System.String</span></span>


## <span data-ttu-id="11278-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="11278-127">OUTPUTS</span></span>

### <span data-ttu-id="11278-128">Microsoft. Azure. Commands. Network. model. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="11278-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="11278-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="11278-129">NOTES</span></span>

## <span data-ttu-id="11278-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="11278-130">RELATED LINKS</span></span>
