---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/set-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Set-AzAnalysisServicesServer.md
ms.openlocfilehash: 05a4ce9fdaeebc447be0d8f1e6162399f964043f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751200"
---
# <span data-ttu-id="1913e-101">Set-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="1913e-101">Set-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="1913e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1913e-102">SYNOPSIS</span></span>
<span data-ttu-id="1913e-103">Analysis Services sunucusu örneğini değiştirir</span><span class="sxs-lookup"><span data-stu-id="1913e-103">Modifies  an instance of Analysis Services server</span></span>

## <span data-ttu-id="1913e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1913e-104">SYNTAX</span></span>

### <span data-ttu-id="1913e-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1913e-105">Default (Default)</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1913e-106">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="1913e-106">DisableBackup</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1913e-107">DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="1913e-107">DisassociateGateway</span></span>
```
Set-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-ReadonlyReplicaCount <Int32>]
 [-DefaultConnectionMode <String>] [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>]
 [-DisassociateGateway] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1913e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1913e-108">DESCRIPTION</span></span>
<span data-ttu-id="1913e-109">Set-AzAnalysisServicesServer cmdlet 'i Analysis Services sunucusunun bir örneğini değiştirir</span><span class="sxs-lookup"><span data-stu-id="1913e-109">The Set-AzAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="1913e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1913e-110">EXAMPLES</span></span>

### <span data-ttu-id="1913e-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1913e-111">Example 1</span></span>
```
PS C:\> Set-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="1913e-112">Anahtar olarak ayarlamak için resourcegroup testgroup içinde TestServer adlı sunucuyu değiştirir testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="1913e-112">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="1913e-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1913e-113">PARAMETERS</span></span>

### <span data-ttu-id="1913e-114">-Yönetici</span><span class="sxs-lookup"><span data-stu-id="1913e-114">-Administrator</span></span>
<span data-ttu-id="1913e-115">Sunucuda yönetici olarak ayarlanacak Kullanıcı veya grupların virgülle ayrılmış listesini temsil eden dize.</span><span class="sxs-lookup"><span data-stu-id="1913e-115">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="1913e-116">Kullanıcıların veya grupların UPN biçiminde ( user@contoso.com veya groups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="1913e-116">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1913e-117">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="1913e-117">-BackupBlobContainerUri</span></span>
<span data-ttu-id="1913e-118">Çözümleme Hizmetleri sunucusunu yedeklemek için blob kapsayıcı URI 'Si</span><span class="sxs-lookup"><span data-stu-id="1913e-118">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1913e-119">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="1913e-119">-DefaultConnectionMode</span></span>
<span data-ttu-id="1913e-120">Çözümleme hizmeti sunucusunun varsayılan bağlantı modu</span><span class="sxs-lookup"><span data-stu-id="1913e-120">Default connection mode of an Analysis service server</span></span>

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

### <span data-ttu-id="1913e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1913e-121">-DefaultProfile</span></span>
<span data-ttu-id="1913e-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1913e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1913e-123">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="1913e-123">-DisableBackup</span></span>
<span data-ttu-id="1913e-124">Yedek blob kapsayıcısını devre dışı bırakma anahtarı.</span><span class="sxs-lookup"><span data-stu-id="1913e-124">The switch to disable backup blob container.</span></span>
<span data-ttu-id="1913e-125">Yedek blob kapsayıcısını yeniden etkinleştirmek için lütfen yedek blob kapsayıcı URI 'sini-BackupBlobContainerUri olarak sağlayın.</span><span class="sxs-lookup"><span data-stu-id="1913e-125">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableBackup
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1913e-126">-DisassociateGateway</span><span class="sxs-lookup"><span data-stu-id="1913e-126">-DisassociateGateway</span></span>
<span data-ttu-id="1913e-127">Ağ Geçidi kaynağının çözümleme sunucusundan ilişkisini kaldırma</span><span class="sxs-lookup"><span data-stu-id="1913e-127">Disassociate Gateway resource from an Analysis server</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisassociateGateway
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1913e-128">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="1913e-128">-FirewallConfig</span></span>
<span data-ttu-id="1913e-129">Çözümleme sunucusunun güvenlik duvarı yapılandırması</span><span class="sxs-lookup"><span data-stu-id="1913e-129">Firewall config of an Analysis server</span></span>

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

### <span data-ttu-id="1913e-130">-Gatewayresourceıd</span><span class="sxs-lookup"><span data-stu-id="1913e-130">-GatewayResourceId</span></span>
<span data-ttu-id="1913e-131">Çözümleme sunucusu için ağ geçidi kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="1913e-131">Gateway resource Id for assocaite to an Analysis server</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1913e-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="1913e-132">-Name</span></span>
<span data-ttu-id="1913e-133">Analysis Services sunucusunun adı</span><span class="sxs-lookup"><span data-stu-id="1913e-133">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="1913e-134">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1913e-134">-PassThru</span></span>
<span data-ttu-id="1913e-135">İşlem başarıyla tamamlandığında silinen sunucu ayrıntılarını döndürür</span><span class="sxs-lookup"><span data-stu-id="1913e-135">Will return the deleted server details if the operation completes successfully</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1913e-136">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="1913e-136">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="1913e-137">Çözümleme hizmeti sunucusunun salt okunur kopya sayısı</span><span class="sxs-lookup"><span data-stu-id="1913e-137">Read only replica count of an Analysis service server</span></span>

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

### <span data-ttu-id="1913e-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1913e-138">-ResourceGroupName</span></span>
<span data-ttu-id="1913e-139">Sunucunun ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="1913e-139">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1913e-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="1913e-140">-Sku</span></span>
<span data-ttu-id="1913e-141">Sunucunun SKU adı.</span><span class="sxs-lookup"><span data-stu-id="1913e-141">The name of the Sku for the server.</span></span>
<span data-ttu-id="1913e-142">Desteklenen değerler, Standart katman için 0 ' ın 1 ' i 1 ' in 2 ' nin 4 ' ü; ' B1 ', temel katman için ' B2 ' ve geliştirme katmanı için 1 '.</span><span class="sxs-lookup"><span data-stu-id="1913e-142">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1913e-143">Etiketli</span><span class="sxs-lookup"><span data-stu-id="1913e-143">-Tag</span></span>
<span data-ttu-id="1913e-144">Sunucuda etiket olarak ayarlanan karma tablo biçimindeki anahtar değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="1913e-144">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1913e-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="1913e-145">-Confirm</span></span>
<span data-ttu-id="1913e-146">Kullanıcıya işlemi gerçekleştirmeyi onaylamanızı ister</span><span class="sxs-lookup"><span data-stu-id="1913e-146">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="1913e-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1913e-147">-WhatIf</span></span>
<span data-ttu-id="1913e-148">Geçerli işlemin gerçekte gerçekleştirmesi gerekmeden gerçekleştireceği işlemleri açıklar</span><span class="sxs-lookup"><span data-stu-id="1913e-148">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="1913e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1913e-149">CommonParameters</span></span>
<span data-ttu-id="1913e-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1913e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1913e-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1913e-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1913e-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1913e-152">INPUTS</span></span>

### <span data-ttu-id="1913e-153">System. String</span><span class="sxs-lookup"><span data-stu-id="1913e-153">System.String</span></span>

### <span data-ttu-id="1913e-154">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1913e-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1913e-155">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1913e-155">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="1913e-156">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1913e-156">System.Int32</span></span>

### <span data-ttu-id="1913e-157">Microsoft. Azure. Commands. AnalysisServices. modeller. Psazureanalysisservices, Allconfig</span><span class="sxs-lookup"><span data-stu-id="1913e-157">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="1913e-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1913e-158">OUTPUTS</span></span>

### <span data-ttu-id="1913e-159">Microsoft. Azure. Commands. AnalysisServices. modeller. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="1913e-159">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="1913e-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1913e-160">NOTES</span></span>
<span data-ttu-id="1913e-161">Diğer ad: Set-AzAs</span><span class="sxs-lookup"><span data-stu-id="1913e-161">Alias: Set-AzAs</span></span>

## <span data-ttu-id="1913e-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1913e-162">RELATED LINKS</span></span>

[<span data-ttu-id="1913e-163">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="1913e-163">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="1913e-164">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="1913e-164">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
