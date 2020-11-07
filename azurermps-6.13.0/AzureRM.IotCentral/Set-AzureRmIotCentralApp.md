---
external help file: Microsoft.Azure.Commands.IotCentral.dll-Help.xml
Module Name: AzureRM.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iotcentral/set-azurermiotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Set-AzureRmIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Set-AzureRmIotCentralApp.md
ms.openlocfilehash: a9b7dbc962809288979f5293c14fd875081f48bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764954"
---
# <span data-ttu-id="dd8c1-101">Set-AzureRmIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="dd8c1-101">Set-AzureRmIotCentralApp</span></span>

## <span data-ttu-id="dd8c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd8c1-102">SYNOPSIS</span></span>
<span data-ttu-id="dd8c1-103">IoT Merkezi uygulaması için meta verileri güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="dd8c1-103">Updates the metadata for an IoT Central Application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd8c1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dd8c1-104">SYNTAX</span></span>

### <span data-ttu-id="dd8c1-105">Resourceıdparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dd8c1-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzureRmIotCentralApp [-DisplayName <String>] [-Tag <Hashtable>] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd8c1-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="dd8c1-106">InputObjectParameterSet</span></span>
```
Set-AzureRmIotCentralApp [-DisplayName <String>] [-Tag <Hashtable>] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd8c1-107">Interactiveıotmerkezileştirme Parametrekümesi</span><span class="sxs-lookup"><span data-stu-id="dd8c1-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzureRmIotCentralApp [-DisplayName <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd8c1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="dd8c1-108">DESCRIPTION</span></span>
<span data-ttu-id="dd8c1-109">IoT Merkezi uygulamasının meta verilerini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="dd8c1-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="dd8c1-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dd8c1-110">EXAMPLES</span></span>

### <span data-ttu-id="dd8c1-111">Örnek 1 güncelleştirme görünen adı</span><span class="sxs-lookup"><span data-stu-id="dd8c1-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="dd8c1-112">Var olan IoT merkezi uygulamasında görünen adı güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="dd8c1-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="dd8c1-113">Örnek çıktı:</span><span class="sxs-lookup"><span data-stu-id="dd8c1-113">Example Output:</span></span>

<span data-ttu-id="dd8c1-114">RESOURCEID:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. Iotcentral/ıotapps/MyAppResourceName adı: MyAppResourceName türü: Microsoft. ıotcentral/ıotapps konumu: westus Tag: SKU: Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX Ida: iotc-default@1.0.0 SubscriptionID: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd8c1-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="dd8c1-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dd8c1-115">PARAMETERS</span></span>

### <span data-ttu-id="dd8c1-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="dd8c1-116">-AsJob</span></span>
<span data-ttu-id="dd8c1-117">Cmdlet 'i arka planda iş olarak çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="dd8c1-117">Run cmdlet as a job in the background.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd8c1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd8c1-118">-DefaultProfile</span></span>
<span data-ttu-id="dd8c1-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dd8c1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd8c1-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="dd8c1-120">-DisplayName</span></span>
<span data-ttu-id="dd8c1-121">IoT Merkezi uygulamasının özel görünen adı.</span><span class="sxs-lookup"><span data-stu-id="dd8c1-121">Custom Display Name of the Iot Central Application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd8c1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd8c1-122">-InputObject</span></span>
<span data-ttu-id="dd8c1-123">IoT Merkezi uygulama giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="dd8c1-123">Iot Central Application Input Object.</span></span>

```yaml
Type: PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd8c1-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="dd8c1-124">-Name</span></span>
<span data-ttu-id="dd8c1-125">IoT Merkezi uygulama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="dd8c1-125">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd8c1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd8c1-126">-ResourceGroupName</span></span>
<span data-ttu-id="dd8c1-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="dd8c1-127">Name of the Resource Group.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd8c1-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="dd8c1-128">-ResourceId</span></span>
<span data-ttu-id="dd8c1-129">IoT Merkezi uygulama kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="dd8c1-129">Iot Central Application Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd8c1-130">Etiketli</span><span class="sxs-lookup"><span data-stu-id="dd8c1-130">-Tag</span></span>
<span data-ttu-id="dd8c1-131">IoT Merkezi uygulama kaynağı etiketleri.</span><span class="sxs-lookup"><span data-stu-id="dd8c1-131">Iot Central Application Resource Tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd8c1-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="dd8c1-132">-Confirm</span></span>
<span data-ttu-id="dd8c1-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dd8c1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd8c1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd8c1-134">-WhatIf</span></span>
<span data-ttu-id="dd8c1-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dd8c1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd8c1-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dd8c1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd8c1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd8c1-137">CommonParameters</span></span>
<span data-ttu-id="dd8c1-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dd8c1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd8c1-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd8c1-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd8c1-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dd8c1-140">INPUTS</span></span>

### <span data-ttu-id="dd8c1-141">System. String</span><span class="sxs-lookup"><span data-stu-id="dd8c1-141">System.String</span></span>
### <span data-ttu-id="dd8c1-142">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="dd8c1-142">System.Collections.Hashtable</span></span>
### <span data-ttu-id="dd8c1-143">Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="dd8c1-143">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="dd8c1-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dd8c1-144">OUTPUTS</span></span>

### <span data-ttu-id="dd8c1-145">Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="dd8c1-145">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="dd8c1-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dd8c1-146">NOTES</span></span>

## <span data-ttu-id="dd8c1-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dd8c1-147">RELATED LINKS</span></span>
