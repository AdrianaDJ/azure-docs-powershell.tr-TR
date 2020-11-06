---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 22B63259-799B-4F25-A06B-7A818D295870
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/reset-azurermservermanagementgatewayprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Reset-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Reset-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: 0833266bcd6e98a1d9744db2bc202bce5a01f3f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588775"
---
# <span data-ttu-id="52f7e-101">Reset-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="52f7e-101">Reset-AzureRmServerManagementGatewayProfile</span></span>

## <span data-ttu-id="52f7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52f7e-102">SYNOPSIS</span></span>
<span data-ttu-id="52f7e-103">Sunucu yönetimi ağ geçidi profilini sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="52f7e-103">Resets the profile of a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52f7e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="52f7e-104">SYNTAX</span></span>

### <span data-ttu-id="52f7e-105">ByName</span><span class="sxs-lookup"><span data-stu-id="52f7e-105">ByName</span></span>
```
Reset-AzureRmServerManagementGatewayProfile [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52f7e-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="52f7e-106">ByObject</span></span>
```
Reset-AzureRmServerManagementGatewayProfile [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="52f7e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="52f7e-107">DESCRIPTION</span></span>
<span data-ttu-id="52f7e-108">**Reset-AzureRmServerManagementGatewayProfile** cmdlet 'i, bir Azure Server yönetim ağ geçidi profilini sıfırlar.</span><span class="sxs-lookup"><span data-stu-id="52f7e-108">The **Reset-AzureRmServerManagementGatewayProfile** cmdlet resets the profile for an Azure Server Management Gateway.</span></span>

<span data-ttu-id="52f7e-109">Profili indirmek için Save-AzureRmServerManagementGatewayProfile cmdlet 'ini kullanmanız ve profili sıfırladıktan sonra kaydetmek için Install-AzureRmServerManagementGatewayProfile cmdlet 'ini kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="52f7e-109">You will need to use the Save-AzureRmServerManagementGatewayProfile cmdlet to download the profile and then the Install-AzureRmServerManagementGatewayProfile cmdlet to save it after you reset the profile.</span></span>

## <span data-ttu-id="52f7e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="52f7e-110">EXAMPLES</span></span>

## <span data-ttu-id="52f7e-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="52f7e-111">PARAMETERS</span></span>

### <span data-ttu-id="52f7e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52f7e-112">-DefaultProfile</span></span>
<span data-ttu-id="52f7e-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="52f7e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52f7e-114">-Ağ Geçidi</span><span class="sxs-lookup"><span data-stu-id="52f7e-114">-Gateway</span></span>
<span data-ttu-id="52f7e-115">Cmdlet 'in profili sıfırlayan ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="52f7e-115">Specifies the gateway for which the cmdlet resets the profile for.</span></span>

<span data-ttu-id="52f7e-116">ResourceGoupName ve GatewayName yerine belirtilebilir</span><span class="sxs-lookup"><span data-stu-id="52f7e-116">May be specified instead of ResourceGoupName and GatewayName</span></span>

```yaml
Type: Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52f7e-117">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="52f7e-117">-GatewayName</span></span>
<span data-ttu-id="52f7e-118">Cmdlet 'in profili sıfırlayan ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="52f7e-118">Specifies the name of the gateway for which the cmdlet resets the profile.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52f7e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52f7e-119">-ResourceGroupName</span></span>
<span data-ttu-id="52f7e-120">Ağ geçidinin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="52f7e-120">Specifies the name of the resource group that the gateway belongs to.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52f7e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52f7e-121">CommonParameters</span></span>
<span data-ttu-id="52f7e-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="52f7e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52f7e-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52f7e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52f7e-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="52f7e-124">INPUTS</span></span>

### <span data-ttu-id="52f7e-125">Geçidi</span><span class="sxs-lookup"><span data-stu-id="52f7e-125">Gateway</span></span>
<span data-ttu-id="52f7e-126">' Ağ Geçidi ' parametresi ardışık düzenin ' Gateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="52f7e-126">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="52f7e-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="52f7e-127">OUTPUTS</span></span>

## <span data-ttu-id="52f7e-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="52f7e-128">NOTES</span></span>

## <span data-ttu-id="52f7e-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="52f7e-129">RELATED LINKS</span></span>

[<span data-ttu-id="52f7e-130">Install-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="52f7e-130">Install-AzureRmServerManagementGatewayProfile</span></span>](./Install-AzureRmServerManagementGatewayProfile.md)

[<span data-ttu-id="52f7e-131">Save-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="52f7e-131">Save-AzureRmServerManagementGatewayProfile</span></span>](./Save-AzureRmServerManagementGatewayProfile.md)


