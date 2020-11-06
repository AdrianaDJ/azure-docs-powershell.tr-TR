---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: ECF85C07-2C9E-487D-A2ED-77875C380244
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Save-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Save-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: af7184b3e43d2016ff4acc9e7634f831945a8fdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593005"
---
# <span data-ttu-id="2767b-101">Save-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="2767b-101">Save-AzureRmServerManagementGatewayProfile</span></span>

## <span data-ttu-id="2767b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2767b-102">SYNOPSIS</span></span>
<span data-ttu-id="2767b-103">Sunucu yönetimi ağ geçidi profilini indirir ve yerel dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="2767b-103">Downloads the profile for a Server Management gateway and saves it to a local file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2767b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2767b-104">SYNTAX</span></span>

### <span data-ttu-id="2767b-105">ByName</span><span class="sxs-lookup"><span data-stu-id="2767b-105">ByName</span></span>
```
Save-AzureRmServerManagementGatewayProfile [-OutputFile] <FileInfo> [-ResourceGroupName] <String>
 [-GatewayName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2767b-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="2767b-106">ByObject</span></span>
```
Save-AzureRmServerManagementGatewayProfile [-OutputFile] <FileInfo> [-Gateway] <Gateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2767b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2767b-107">DESCRIPTION</span></span>
<span data-ttu-id="2767b-108">**Save-AzureRmServerManagementGatewayProfile** cmdlet 'i, bir Azure Server yönetim ağ geçidi profilini indirir ve yerel dosyaya depolar.</span><span class="sxs-lookup"><span data-stu-id="2767b-108">The **Save-AzureRmServerManagementGatewayProfile** cmdlet downloads the profile for an Azure Server Management gateway and stores it to a local file.</span></span>

## <span data-ttu-id="2767b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2767b-109">EXAMPLES</span></span>

## <span data-ttu-id="2767b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2767b-110">PARAMETERS</span></span>

### <span data-ttu-id="2767b-111">-Ağ Geçidi</span><span class="sxs-lookup"><span data-stu-id="2767b-111">-Gateway</span></span>
<span data-ttu-id="2767b-112">Bu cmdlet 'in profili aldığı ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2767b-112">Specifies the gateway that this cmdlet gets the profile for.</span></span>

<span data-ttu-id="2767b-113">ResourceGroupName ve GatewayName belirtmek yerine kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="2767b-113">May be used instead of specifying ResourceGroupName and GatewayName</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2767b-114">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="2767b-114">-GatewayName</span></span>
<span data-ttu-id="2767b-115">Bu cmdlet 'in profili aldığı ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2767b-115">Specifies the name of the gateway that this cmdlet gets the profile for.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2767b-116">-ÇıktıDosyası</span><span class="sxs-lookup"><span data-stu-id="2767b-116">-OutputFile</span></span>
<span data-ttu-id="2767b-117">Profil verilerinin kaydedileceği yerel dosyayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="2767b-117">Specifies the local file in which to save the profile data.</span></span>

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2767b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2767b-118">-ResourceGroupName</span></span>
<span data-ttu-id="2767b-119">Ağ geçidinin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2767b-119">Specifies the name of the resource group that the gateway belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2767b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2767b-120">-DefaultProfile</span></span>
<span data-ttu-id="2767b-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2767b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2767b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2767b-122">CommonParameters</span></span>
<span data-ttu-id="2767b-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2767b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2767b-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2767b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2767b-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2767b-125">INPUTS</span></span>

### <span data-ttu-id="2767b-126">Geçidi</span><span class="sxs-lookup"><span data-stu-id="2767b-126">Gateway</span></span>
<span data-ttu-id="2767b-127">' Ağ Geçidi ' parametresi ardışık düzenin ' Gateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="2767b-127">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="2767b-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2767b-128">OUTPUTS</span></span>

### <span data-ttu-id="2767b-129">System. ıO. FILEINFO</span><span class="sxs-lookup"><span data-stu-id="2767b-129">System.IO.FileInfo</span></span>

## <span data-ttu-id="2767b-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2767b-130">NOTES</span></span>

## <span data-ttu-id="2767b-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2767b-131">RELATED LINKS</span></span>

[<span data-ttu-id="2767b-132">Install-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="2767b-132">Install-AzureRmServerManagementGatewayProfile</span></span>](./Install-AzureRmServerManagementGatewayProfile.md)

[<span data-ttu-id="2767b-133">Reset-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="2767b-133">Reset-AzureRmServerManagementGatewayProfile</span></span>](./Reset-AzureRmServerManagementGatewayProfile.md)


