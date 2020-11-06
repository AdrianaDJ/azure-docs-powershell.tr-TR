---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 6bda63ad0c8e900a73c0ccd2afc506be7feae908
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587056"
---
# <span data-ttu-id="94d62-101">Set-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="94d62-101">Set-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="94d62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94d62-102">SYNOPSIS</span></span>
<span data-ttu-id="94d62-103">Analysis Services sunucusu örneğini değiştirir</span><span class="sxs-lookup"><span data-stu-id="94d62-103">Modifies  an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94d62-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="94d62-104">SYNTAX</span></span>

### <span data-ttu-id="94d62-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="94d62-105">Default (Default)</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94d62-106">Yedeği devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="94d62-106">Disable Backup</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94d62-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="94d62-107">DESCRIPTION</span></span>
<span data-ttu-id="94d62-108">Set-AzureRmAnalysisServicesServer cmdlet 'i Analysis Services sunucusunun bir örneğini değiştirir</span><span class="sxs-lookup"><span data-stu-id="94d62-108">The Set-AzureRmAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="94d62-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="94d62-109">EXAMPLES</span></span>

### <span data-ttu-id="94d62-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="94d62-110">Example 1</span></span>
```
PS C:\> Set-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="94d62-111">Anahtar olarak ayarlamak için resourcegroup testgroup içinde TestServer adlı sunucuyu değiştirir testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d62-111">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="94d62-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="94d62-112">PARAMETERS</span></span>

### <span data-ttu-id="94d62-113">-Yönetici</span><span class="sxs-lookup"><span data-stu-id="94d62-113">-Administrator</span></span>
<span data-ttu-id="94d62-114">Sunucuda yönetici olarak ayarlanacak Kullanıcı veya grupların virgülle ayrılmış listesini temsil eden dize.</span><span class="sxs-lookup"><span data-stu-id="94d62-114">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="94d62-115">Kullanıcıların veya grupların UPN biçiminde ( user@contoso.com veya groups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="94d62-115">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

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

### <span data-ttu-id="94d62-116">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="94d62-116">-BackupBlobContainerUri</span></span>
<span data-ttu-id="94d62-117">Çözümleme Hizmetleri sunucusunu yedeklemek için blob kapsayıcı URI 'Si</span><span class="sxs-lookup"><span data-stu-id="94d62-117">The blob container Uri for backup the Analysis Services server</span></span>

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

### <span data-ttu-id="94d62-118">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="94d62-118">-DisableBackup</span></span>
<span data-ttu-id="94d62-119">Yedek blob kapsayıcısını devre dışı bırakma anahtarı.</span><span class="sxs-lookup"><span data-stu-id="94d62-119">The switch to disable backup blob container.</span></span>
<span data-ttu-id="94d62-120">Yedek blob kapsayıcısını yeniden etkinleştirmek için lütfen yedek blob kapsayıcı URI 'sini-BackupBlobContainerUri olarak sağlayın.</span><span class="sxs-lookup"><span data-stu-id="94d62-120">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable Backup
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94d62-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="94d62-121">-Name</span></span>
<span data-ttu-id="94d62-122">Analysis Services sunucusunun adı</span><span class="sxs-lookup"><span data-stu-id="94d62-122">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="94d62-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="94d62-123">-PassThru</span></span>
<span data-ttu-id="94d62-124">İşlem başarıyla tamamlandığında silinen sunucu ayrıntılarını döndürür</span><span class="sxs-lookup"><span data-stu-id="94d62-124">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="94d62-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94d62-125">-ResourceGroupName</span></span>
<span data-ttu-id="94d62-126">Sunucunun ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="94d62-126">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="94d62-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="94d62-127">-Sku</span></span>
<span data-ttu-id="94d62-128">Sunucunun SKU adı.</span><span class="sxs-lookup"><span data-stu-id="94d62-128">The name of the Sku for the server.</span></span>
<span data-ttu-id="94d62-129">Desteklenen değerler, Standart katman için 0 ' ın 1 ' i 1 ' in 2 ' nin 4 ' ü; ' B1 ', temel katman için ' B2 ' ve geliştirme katmanı için 1 '.</span><span class="sxs-lookup"><span data-stu-id="94d62-129">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

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

### <span data-ttu-id="94d62-130">Etiketli</span><span class="sxs-lookup"><span data-stu-id="94d62-130">-Tag</span></span>
<span data-ttu-id="94d62-131">Sunucuda etiket olarak ayarlanan karma tablo biçimindeki anahtar değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="94d62-131">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

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

### <span data-ttu-id="94d62-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="94d62-132">-Confirm</span></span>
<span data-ttu-id="94d62-133">Kullanıcıya işlemi gerçekleştirmeyi onaylamanızı ister</span><span class="sxs-lookup"><span data-stu-id="94d62-133">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="94d62-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94d62-134">-WhatIf</span></span>
<span data-ttu-id="94d62-135">Geçerli işlemin gerçekte gerçekleştirmesi gerekmeden gerçekleştireceği işlemleri açıklar</span><span class="sxs-lookup"><span data-stu-id="94d62-135">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="94d62-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94d62-136">-DefaultProfile</span></span>
<span data-ttu-id="94d62-137">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="94d62-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94d62-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94d62-138">CommonParameters</span></span>
<span data-ttu-id="94d62-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="94d62-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94d62-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94d62-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94d62-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="94d62-141">INPUTS</span></span>

## <span data-ttu-id="94d62-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="94d62-142">OUTPUTS</span></span>

### <span data-ttu-id="94d62-143">Microsoft. Azure. Management. Analysis. modeller. AnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="94d62-143">Microsoft.Azure.Management.Analysis.Models.AnalysisServicesServer</span></span>

## <span data-ttu-id="94d62-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="94d62-144">NOTES</span></span>
<span data-ttu-id="94d62-145">Diğer ad: Set-AzureAs</span><span class="sxs-lookup"><span data-stu-id="94d62-145">Alias: Set-AzureAs</span></span>

## <span data-ttu-id="94d62-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="94d62-146">RELATED LINKS</span></span>

[<span data-ttu-id="94d62-147">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="94d62-147">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="94d62-148">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="94d62-148">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
