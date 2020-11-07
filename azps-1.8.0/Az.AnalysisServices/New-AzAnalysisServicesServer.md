---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesServer.md
ms.openlocfilehash: 61c5fc7f80ab157724156d86a5cbb8df8bb23841
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751207"
---
# <span data-ttu-id="6a33c-101">New-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="6a33c-101">New-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="6a33c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a33c-102">SYNOPSIS</span></span>
<span data-ttu-id="6a33c-103">Yeni bir Analysis Services sunucusu oluşturur</span><span class="sxs-lookup"><span data-stu-id="6a33c-103">Creates a new Analysis Services server</span></span>

## <span data-ttu-id="6a33c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6a33c-104">SYNTAX</span></span>

```
New-AzAnalysisServicesServer [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a33c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6a33c-105">DESCRIPTION</span></span>
<span data-ttu-id="6a33c-106">New-AzAnalysisServicesServer cmdlet 'i yeni bir Analysis Services sunucusu oluşturur</span><span class="sxs-lookup"><span data-stu-id="6a33c-106">The New-AzAnalysisServicesServer cmdlet creates a new Analysis Services server</span></span>

## <span data-ttu-id="6a33c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6a33c-107">EXAMPLES</span></span>

### <span data-ttu-id="6a33c-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6a33c-108">Example 1</span></span>
```
PS C:\> New-AzAnalysisServicesServer -ResourceGroupName "testresourcegroup" -Name "testserver" -Location "West-US" -Sku "S1"
```

<span data-ttu-id="6a33c-109">A-US ve kaynak grubu testresrourcegroup 'ta TestServer adlı bir sunucu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6a33c-109">Creates a server named testserver in the Azure region West-US and in resource group testresrourcegroup.</span></span> <span data-ttu-id="6a33c-110">Sunucu için SKU düzeyi S1 olacaktır.</span><span class="sxs-lookup"><span data-stu-id="6a33c-110">The sku level for the server will be S1.</span></span>

## <span data-ttu-id="6a33c-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6a33c-111">PARAMETERS</span></span>

### <span data-ttu-id="6a33c-112">-Yönetici</span><span class="sxs-lookup"><span data-stu-id="6a33c-112">-Administrator</span></span>
<span data-ttu-id="6a33c-113">Sunucuda yönetici olarak ayarlanacak Kullanıcı veya grupların virgülle ayrılmış listesini temsil eden dize.</span><span class="sxs-lookup"><span data-stu-id="6a33c-113">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span> <span data-ttu-id="6a33c-114">Kullanıcıların veya grupların UPN biçiminde ( user@contoso.com veya groups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="6a33c-114">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a33c-115">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="6a33c-115">-BackupBlobContainerUri</span></span>
<span data-ttu-id="6a33c-116">Çözümleme Hizmetleri sunucusunu yedeklemek için blob kapsayıcı URI 'Si</span><span class="sxs-lookup"><span data-stu-id="6a33c-116">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a33c-117">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="6a33c-117">-DefaultConnectionMode</span></span>
<span data-ttu-id="6a33c-118">Çözümleme hizmeti sunucusunun varsayılan bağlantı modu</span><span class="sxs-lookup"><span data-stu-id="6a33c-118">Default connection mode of an Analysis service server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: All, Readonly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a33c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a33c-119">-DefaultProfile</span></span>
<span data-ttu-id="6a33c-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6a33c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a33c-121">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="6a33c-121">-FirewallConfig</span></span>
<span data-ttu-id="6a33c-122">Çözümleme sunucusunun güvenlik duvarı yapılandırması</span><span class="sxs-lookup"><span data-stu-id="6a33c-122">Firewall config of an Analysis server</span></span>

```yaml
Type: Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a33c-123">-Gatewayresourceıd</span><span class="sxs-lookup"><span data-stu-id="6a33c-123">-GatewayResourceId</span></span>
<span data-ttu-id="6a33c-124">Çözümleme sunucusu için ağ geçidi kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="6a33c-124">Gateway resource Id for assocaite to an Analysis server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a33c-125">-Konum</span><span class="sxs-lookup"><span data-stu-id="6a33c-125">-Location</span></span>
<span data-ttu-id="6a33c-126">Analysis Services sunucusunun barındırıldığı Azure bölgesi</span><span class="sxs-lookup"><span data-stu-id="6a33c-126">The Azure region where the Analysis Services server is hosted</span></span>

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

### <span data-ttu-id="6a33c-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="6a33c-127">-Name</span></span>
<span data-ttu-id="6a33c-128">Analysis Services sunucusunun adı</span><span class="sxs-lookup"><span data-stu-id="6a33c-128">Name of the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a33c-129">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="6a33c-129">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="6a33c-130">Çözümleme hizmeti sunucusunun salt okunur kopya sayısı</span><span class="sxs-lookup"><span data-stu-id="6a33c-130">Read only replica count of an Analysis service server</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a33c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a33c-131">-ResourceGroupName</span></span>
<span data-ttu-id="6a33c-132">Sunucunun ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="6a33c-132">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="6a33c-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="6a33c-133">-Sku</span></span>
<span data-ttu-id="6a33c-134">Sunucunun SKU adı.</span><span class="sxs-lookup"><span data-stu-id="6a33c-134">The name of the Sku for the server.</span></span>
<span data-ttu-id="6a33c-135">Desteklenen değerler, Standart katman için 0 ' ın 1 ' i 1 ' in 2 ' nin 4 ' ü; ' B1 ', temel katman için ' B2 ' ve geliştirme katmanı için 1 '.</span><span class="sxs-lookup"><span data-stu-id="6a33c-135">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a33c-136">Etiketli</span><span class="sxs-lookup"><span data-stu-id="6a33c-136">-Tag</span></span>
<span data-ttu-id="6a33c-137">Sunucuda etiket olarak ayarlanan karma tablo biçimindeki anahtar değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="6a33c-137">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a33c-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="6a33c-138">-Confirm</span></span>
<span data-ttu-id="6a33c-139">Kullanıcıya işlemi gerçekleştirmeyi onaylamanızı ister</span><span class="sxs-lookup"><span data-stu-id="6a33c-139">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="6a33c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a33c-140">-WhatIf</span></span>
<span data-ttu-id="6a33c-141">Geçerli işlemin gerçekte gerçekleştirmesi gerekmeden gerçekleştireceği işlemleri açıklar</span><span class="sxs-lookup"><span data-stu-id="6a33c-141">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="6a33c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a33c-142">CommonParameters</span></span>
<span data-ttu-id="6a33c-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6a33c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a33c-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a33c-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a33c-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6a33c-145">INPUTS</span></span>

### <span data-ttu-id="6a33c-146">System. String</span><span class="sxs-lookup"><span data-stu-id="6a33c-146">System.String</span></span>

### <span data-ttu-id="6a33c-147">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6a33c-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6a33c-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="6a33c-148">System.Int32</span></span>

### <span data-ttu-id="6a33c-149">Microsoft. Azure. Commands. AnalysisServices. modeller. Psazureanalysisservices, Allconfig</span><span class="sxs-lookup"><span data-stu-id="6a33c-149">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="6a33c-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6a33c-150">OUTPUTS</span></span>

### <span data-ttu-id="6a33c-151">Microsoft. Azure. Commands. AnalysisServices. modeller. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="6a33c-151">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="6a33c-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6a33c-152">NOTES</span></span>
<span data-ttu-id="6a33c-153">Diğer ad: New-AzAs</span><span class="sxs-lookup"><span data-stu-id="6a33c-153">Alias: New-AzAs</span></span>

## <span data-ttu-id="6a33c-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6a33c-154">RELATED LINKS</span></span>

[<span data-ttu-id="6a33c-155">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="6a33c-155">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="6a33c-156">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="6a33c-156">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
