---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
ms.openlocfilehash: 10c9c634d1435e9460b72bfd1ccdb7e77f7fea53
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096073"
---
# <span data-ttu-id="b48c3-101">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="b48c3-101">Set-AzServiceFabricSetting</span></span>

## <span data-ttu-id="b48c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b48c3-102">SYNOPSIS</span></span>
<span data-ttu-id="b48c3-103">Kümeye bir veya birden çok hizmet yapısı ayarı ekleyin veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="b48c3-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

## <span data-ttu-id="b48c3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b48c3-104">SYNTAX</span></span>

### <span data-ttu-id="b48c3-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="b48c3-105">OneSetting</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String> -Parameter <String>
 -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b48c3-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="b48c3-106">BatchSettings</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b48c3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b48c3-107">DESCRIPTION</span></span>
<span data-ttu-id="b48c3-108">Kümedeki hizmet doku ayarlarını eklemek veya güncelleştirmek için **set-AzServiceFabricSetting** kullanın.</span><span class="sxs-lookup"><span data-stu-id="b48c3-108">Use **Set-AzServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="b48c3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b48c3-109">EXAMPLES</span></span>

### <span data-ttu-id="b48c3-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b48c3-110">Example 1</span></span>
```
PS c:\> Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="b48c3-111">Bu komut, ' NamingService ' bölümünün altındaki ' MaxFileOperationTimeout ' değerini ' 5000 ' olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b48c3-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>

## <span data-ttu-id="b48c3-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b48c3-112">PARAMETERS</span></span>

### <span data-ttu-id="b48c3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b48c3-113">-DefaultProfile</span></span>
<span data-ttu-id="b48c3-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b48c3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b48c3-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="b48c3-115">-Name</span></span>
<span data-ttu-id="b48c3-116">Kümenin adını belirtme</span><span class="sxs-lookup"><span data-stu-id="b48c3-116">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b48c3-117">-Parametre</span><span class="sxs-lookup"><span data-stu-id="b48c3-117">-Parameter</span></span>
<span data-ttu-id="b48c3-118">Doku ayarının parametre adı</span><span class="sxs-lookup"><span data-stu-id="b48c3-118">Parameter name of the fabric setting</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b48c3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b48c3-119">-ResourceGroupName</span></span>
<span data-ttu-id="b48c3-120">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="b48c3-120">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b48c3-121">-Bölüm</span><span class="sxs-lookup"><span data-stu-id="b48c3-121">-Section</span></span>
<span data-ttu-id="b48c3-122">Doku ayarının bölüm adı</span><span class="sxs-lookup"><span data-stu-id="b48c3-122">Section name of the fabric setting</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b48c3-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="b48c3-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="b48c3-124">Doku ayarları dizisi</span><span class="sxs-lookup"><span data-stu-id="b48c3-124">An array of fabric settings</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]
Parameter Sets: BatchSettings
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b48c3-125">-Değer</span><span class="sxs-lookup"><span data-stu-id="b48c3-125">-Value</span></span>
<span data-ttu-id="b48c3-126">Doku ayarının parametre değeri</span><span class="sxs-lookup"><span data-stu-id="b48c3-126">Parameter value of the fabric setting</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b48c3-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="b48c3-127">-Confirm</span></span>
<span data-ttu-id="b48c3-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b48c3-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b48c3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b48c3-129">-WhatIf</span></span>
<span data-ttu-id="b48c3-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b48c3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b48c3-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b48c3-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b48c3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b48c3-132">CommonParameters</span></span>
<span data-ttu-id="b48c3-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b48c3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b48c3-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b48c3-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b48c3-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b48c3-135">INPUTS</span></span>

### <span data-ttu-id="b48c3-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b48c3-136">System.String</span></span>

### <span data-ttu-id="b48c3-137">Microsoft. Azure. Commands. ServiceFabric. modeller. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="b48c3-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="b48c3-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b48c3-138">OUTPUTS</span></span>

### <span data-ttu-id="b48c3-139">Microsoft. Azure. Commands. ServiceFabric. modeller. PSCluster</span><span class="sxs-lookup"><span data-stu-id="b48c3-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="b48c3-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b48c3-140">NOTES</span></span>

## <span data-ttu-id="b48c3-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b48c3-141">RELATED LINKS</span></span>
