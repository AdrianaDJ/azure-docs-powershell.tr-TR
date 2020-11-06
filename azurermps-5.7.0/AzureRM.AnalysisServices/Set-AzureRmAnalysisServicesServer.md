---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/set-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 485687b0a08ca69edc77b4ee5f9510ad8a1396a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588223"
---
# <span data-ttu-id="b6587-101">Set-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="b6587-101">Set-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="b6587-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6587-102">SYNOPSIS</span></span>
<span data-ttu-id="b6587-103">Analysis Services sunucusu örneğini değiştirir</span><span class="sxs-lookup"><span data-stu-id="b6587-103">Modifies  an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6587-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b6587-104">SYNTAX</span></span>

### <span data-ttu-id="b6587-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b6587-105">Default (Default)</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6587-106">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="b6587-106">DisableBackup</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6587-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b6587-107">DESCRIPTION</span></span>
<span data-ttu-id="b6587-108">Set-AzureRmAnalysisServicesServer cmdlet 'i Analysis Services sunucusunun bir örneğini değiştirir</span><span class="sxs-lookup"><span data-stu-id="b6587-108">The Set-AzureRmAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="b6587-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b6587-109">EXAMPLES</span></span>

### <span data-ttu-id="b6587-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b6587-110">Example 1</span></span>
```
PS C:\> Set-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="b6587-111">Anahtar olarak ayarlamak için resourcegroup testgroup içinde TestServer adlı sunucuyu değiştirir testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="b6587-111">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="b6587-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b6587-112">PARAMETERS</span></span>

### <span data-ttu-id="b6587-113">-Yönetici</span><span class="sxs-lookup"><span data-stu-id="b6587-113">-Administrator</span></span>
<span data-ttu-id="b6587-114">Sunucuda yönetici olarak ayarlanacak Kullanıcı veya grupların virgülle ayrılmış listesini temsil eden dize.</span><span class="sxs-lookup"><span data-stu-id="b6587-114">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="b6587-115">Kullanıcıların veya grupların UPN biçiminde ( user@contoso.com veya groups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="b6587-115">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6587-116">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="b6587-116">-BackupBlobContainerUri</span></span>
<span data-ttu-id="b6587-117">Çözümleme Hizmetleri sunucusunu yedeklemek için blob kapsayıcı URI 'Si</span><span class="sxs-lookup"><span data-stu-id="b6587-117">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6587-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6587-118">-DefaultProfile</span></span>
<span data-ttu-id="b6587-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b6587-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6587-120">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="b6587-120">-DisableBackup</span></span>
<span data-ttu-id="b6587-121">Yedek blob kapsayıcısını devre dışı bırakma anahtarı.</span><span class="sxs-lookup"><span data-stu-id="b6587-121">The switch to disable backup blob container.</span></span>
<span data-ttu-id="b6587-122">Yedek blob kapsayıcısını yeniden etkinleştirmek için lütfen yedek blob kapsayıcı URI 'sini-BackupBlobContainerUri olarak sağlayın.</span><span class="sxs-lookup"><span data-stu-id="b6587-122">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableBackup
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6587-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="b6587-123">-Name</span></span>
<span data-ttu-id="b6587-124">Analysis Services sunucusunun adı</span><span class="sxs-lookup"><span data-stu-id="b6587-124">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="b6587-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b6587-125">-PassThru</span></span>
<span data-ttu-id="b6587-126">İşlem başarıyla tamamlandığında silinen sunucu ayrıntılarını döndürür</span><span class="sxs-lookup"><span data-stu-id="b6587-126">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="b6587-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6587-127">-ResourceGroupName</span></span>
<span data-ttu-id="b6587-128">Sunucunun ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="b6587-128">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6587-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="b6587-129">-Sku</span></span>
<span data-ttu-id="b6587-130">Sunucunun SKU adı.</span><span class="sxs-lookup"><span data-stu-id="b6587-130">The name of the Sku for the server.</span></span>
<span data-ttu-id="b6587-131">Desteklenen değerler, Standart katman için 0 ' ın 1 ' i 1 ' in 2 ' nin 4 ' ü; ' B1 ', temel katman için ' B2 ' ve geliştirme katmanı için 1 '.</span><span class="sxs-lookup"><span data-stu-id="b6587-131">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6587-132">Etiketli</span><span class="sxs-lookup"><span data-stu-id="b6587-132">-Tag</span></span>
<span data-ttu-id="b6587-133">Sunucuda etiket olarak ayarlanan karma tablo biçimindeki anahtar değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="b6587-133">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6587-134">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="b6587-134">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="b6587-135">Çözümleme hizmeti sunucusunun salt okunur kopya sayısı</span><span class="sxs-lookup"><span data-stu-id="b6587-135">Read only replica count of an Analysis service server</span></span>

```yaml
Type: Integer
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6587-136">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="b6587-136">-DefaultConnectionMode</span></span>
<span data-ttu-id="b6587-137">Çözümleme hizmeti sunucusunun varsayılan bağlantı modu</span><span class="sxs-lookup"><span data-stu-id="b6587-137">Default connection mode of an Analysis service server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6587-138">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="b6587-138">-FirewallConfig</span></span>
<span data-ttu-id="b6587-139">Çözümleme sunucusunun güvenlik duvarı yapılandırması</span><span class="sxs-lookup"><span data-stu-id="b6587-139">Firewall config of an Analysis server</span></span>

```yaml
Type: Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6587-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="b6587-140">-Confirm</span></span>
<span data-ttu-id="b6587-141">Kullanıcıya işlemi gerçekleştirmeyi onaylamanızı ister</span><span class="sxs-lookup"><span data-stu-id="b6587-141">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="b6587-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6587-142">-WhatIf</span></span>
<span data-ttu-id="b6587-143">Geçerli işlemin gerçekte gerçekleştirmesi gerekmeden gerçekleştireceği işlemleri açıklar</span><span class="sxs-lookup"><span data-stu-id="b6587-143">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="b6587-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6587-144">CommonParameters</span></span>
<span data-ttu-id="b6587-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b6587-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6587-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6587-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6587-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b6587-147">INPUTS</span></span>

### <span data-ttu-id="b6587-148">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b6587-148">None</span></span>
<span data-ttu-id="b6587-149">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="b6587-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b6587-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b6587-150">OUTPUTS</span></span>

### <span data-ttu-id="b6587-151">Microsoft. Azure. Management. Analysis. modeller. AnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="b6587-151">Microsoft.Azure.Management.Analysis.Models.AnalysisServicesServer</span></span>

## <span data-ttu-id="b6587-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b6587-152">NOTES</span></span>
<span data-ttu-id="b6587-153">Diğer ad: Set-AzureAs</span><span class="sxs-lookup"><span data-stu-id="b6587-153">Alias: Set-AzureAs</span></span>

## <span data-ttu-id="b6587-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b6587-154">RELATED LINKS</span></span>

[<span data-ttu-id="b6587-155">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="b6587-155">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="b6587-156">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="b6587-156">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
