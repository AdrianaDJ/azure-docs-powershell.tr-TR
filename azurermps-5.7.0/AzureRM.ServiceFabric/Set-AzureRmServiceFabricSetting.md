---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/set-azurermservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricSetting.md
ms.openlocfilehash: 8296945de2bcf98213fc692e486e793a91f84939
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587426"
---
# <span data-ttu-id="05848-101">Set-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="05848-101">Set-AzureRmServiceFabricSetting</span></span>

## <span data-ttu-id="05848-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05848-102">SYNOPSIS</span></span>
<span data-ttu-id="05848-103">Kümeye bir veya birden çok hizmet yapısı ayarı ekleyin veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="05848-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05848-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="05848-104">SYNTAX</span></span>

### <span data-ttu-id="05848-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="05848-105">OneSetting</span></span>
```
Set-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="05848-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="05848-106">BatchSettings</span></span>
```
Set-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05848-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="05848-107">DESCRIPTION</span></span>
<span data-ttu-id="05848-108">Kümeye hizmet yapısı ayarları eklemek veya bunları güncelleştirmek için **set-AzureRmServiceFabricSetting** kullanın.</span><span class="sxs-lookup"><span data-stu-id="05848-108">Use **Set-AzureRmServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="05848-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="05848-109">EXAMPLES</span></span>

### <span data-ttu-id="05848-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="05848-110">Example 1</span></span>
```
PS c:\> Set-AzureRmServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="05848-111">Bu komut, ' NamingService ' bölümünün altındaki ' MaxFileOperationTimeout ' değerini ' 5000 ' olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="05848-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>

## <span data-ttu-id="05848-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="05848-112">PARAMETERS</span></span>

### <span data-ttu-id="05848-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05848-113">-DefaultProfile</span></span>
<span data-ttu-id="05848-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="05848-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05848-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="05848-115">-Name</span></span>
<span data-ttu-id="05848-116">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="05848-116">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05848-117">-Parametre</span><span class="sxs-lookup"><span data-stu-id="05848-117">-Parameter</span></span>
<span data-ttu-id="05848-118">Parametresi.</span><span class="sxs-lookup"><span data-stu-id="05848-118">Parameter.</span></span>

```yaml
Type: String
Parameter Sets: OneSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05848-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05848-119">-ResourceGroupName</span></span>
<span data-ttu-id="05848-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="05848-120">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05848-121">-Bölüm</span><span class="sxs-lookup"><span data-stu-id="05848-121">-Section</span></span>
<span data-ttu-id="05848-122">Bölümde.</span><span class="sxs-lookup"><span data-stu-id="05848-122">Section.</span></span>

```yaml
Type: String
Parameter Sets: OneSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05848-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="05848-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="05848-124">İstemci kimlik doğrulama türü.</span><span class="sxs-lookup"><span data-stu-id="05848-124">Client authentication type.</span></span>

```yaml
Type: PSSettingsSectionDescription[]
Parameter Sets: BatchSettings
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05848-125">-Değer</span><span class="sxs-lookup"><span data-stu-id="05848-125">-Value</span></span>
<span data-ttu-id="05848-126">Değerlerini.</span><span class="sxs-lookup"><span data-stu-id="05848-126">Value.</span></span>

```yaml
Type: String
Parameter Sets: OneSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05848-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="05848-127">-Confirm</span></span>
<span data-ttu-id="05848-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="05848-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05848-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05848-129">-WhatIf</span></span>
<span data-ttu-id="05848-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="05848-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="05848-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="05848-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05848-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05848-132">CommonParameters</span></span>
<span data-ttu-id="05848-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="05848-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05848-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05848-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05848-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="05848-135">INPUTS</span></span>

### <span data-ttu-id="05848-136">System. String</span><span class="sxs-lookup"><span data-stu-id="05848-136">System.String</span></span>
<span data-ttu-id="05848-137">Microsoft. Azure. Commands. ServiceFabric. modeller. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="05848-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="05848-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="05848-138">OUTPUTS</span></span>

### <span data-ttu-id="05848-139">Microsoft. Azure. Commands. ServiceFabric. modeller. PsCluster</span><span class="sxs-lookup"><span data-stu-id="05848-139">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="05848-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="05848-140">NOTES</span></span>

## <span data-ttu-id="05848-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="05848-141">RELATED LINKS</span></span>

