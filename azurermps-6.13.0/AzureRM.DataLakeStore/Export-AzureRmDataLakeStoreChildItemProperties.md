---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azureatalakestorechilditemproperties
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreChildItemProperties.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreChildItemProperties.md
ms.openlocfilehash: faaf8a0c614a1243a3e3812cd0b6e1202cc7e75b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591984"
---
# <span data-ttu-id="902f3-101">Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="902f3-101">Export-AzureRmDataLakeStoreChildItemProperties</span></span>

## <span data-ttu-id="902f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="902f3-102">SYNOPSIS</span></span>
<span data-ttu-id="902f3-103">Belirtilen yoldan bir ouput yoluna tüm ağacın özelliklerini (disk kullanımı ve ACL) dışarı aktarır</span><span class="sxs-lookup"><span data-stu-id="902f3-103">Exports the properties (Disk usage and Acl) for the entire tree from the specified path to a ouput path</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="902f3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="902f3-104">SYNTAX</span></span>

### <span data-ttu-id="902f3-105">GetDiskUsage</span><span class="sxs-lookup"><span data-stu-id="902f3-105">GetDiskUsage</span></span>
```
Export-AzureRmDataLakeStoreChildItemProperties [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="902f3-106">GetAllProperties</span><span class="sxs-lookup"><span data-stu-id="902f3-106">GetAllProperties</span></span>
```
Export-AzureRmDataLakeStoreChildItemProperties [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-GetAcl] [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="902f3-107">GetAclDump</span><span class="sxs-lookup"><span data-stu-id="902f3-107">GetAclDump</span></span>
```
Export-AzureRmDataLakeStoreChildItemProperties [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>] [-GetAcl]
 [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="902f3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="902f3-108">DESCRIPTION</span></span>
<span data-ttu-id="902f3-109">**Export-AzureRmDataLakeStoreChildItemProperties** , verilen dizin için ADLS alanı kullanımı veya/ve ACL kullanımını raporlamak üzere kullanılır ve alt dizinleri ve dosyaları.</span><span class="sxs-lookup"><span data-stu-id="902f3-109">The **Export-AzureRmDataLakeStoreChildItemProperties** is used to report the ADLS space usage or/and ACL usage for the given directory and it's sub directories and files.</span></span>

## <span data-ttu-id="902f3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="902f3-110">EXAMPLES</span></span>

### <span data-ttu-id="902f3-111">Örnek 1: tüm alt dizinler ve dosyalar için disk kullanımı ve ACL kullanımını alma</span><span class="sxs-lookup"><span data-stu-id="902f3-111">Example 1: Get the disk usage and ACL usage for all subdirectories and files</span></span>
```
PS C:\> Export-AzureRmDataLakeStoreChildItemProperties -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -GetDiskUsage -IncludeFile
```

<span data-ttu-id="902f3-112">/A'in altındaki tüm alt dizinler ve dosyalar için disk kullanımı ve ACL kullanımını edinin.</span><span class="sxs-lookup"><span data-stu-id="902f3-112">Get the disk usage and ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="902f3-113">Includefile, dosyaların Ayrıca</span><span class="sxs-lookup"><span data-stu-id="902f3-113">IncludeFile ensures the usage is reported for files also</span></span>

### <span data-ttu-id="902f3-114">Örnek 2: tutarlı ACL 'ye sahip tüm alt dizinlerin ve dosyaların ACL kullanımını alma</span><span class="sxs-lookup"><span data-stu-id="902f3-114">Example 2: Get the ACL usage for all subdirectories and files with the consistent ACL hidden</span></span>
```
PS C:\> $fullAcl="user:contoso-userid:--x|user::rwx|other::---|group::rwx"
PS C:\> $newFullAcl = $fullAcl.Split("{|}");
PS C:\> Set-AzureRmDataLakeStoreItemAcl -Account ContosoADL -Path /a -Acl $newFullAcl -Recurse -Debug

PS C:\> Export-AzureRmDataLakeStoreChildItemProperties -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -HideConsistentAcl -IncludeFile
```

<span data-ttu-id="902f3-115">Tüm alt dizinlerin ve/A'in altındaki dosyaların ACL kullanımını edinin.</span><span class="sxs-lookup"><span data-stu-id="902f3-115">Get the ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="902f3-116">Includefile, dosyaların da bu şekilde raporlanmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="902f3-116">IncludeFile ensures the usage is reported for files also.</span></span> <span data-ttu-id="902f3-117">Bu durumda Hidelıtentacl, tüm alt öğelerin/aile aynı ACL 'e sahip olduğu için, alt öğelerin ACL 'sini gösterir.</span><span class="sxs-lookup"><span data-stu-id="902f3-117">HideconsistentAcl in this case will show the Acl of /a, not it's children since all of the children has same acl as /a.</span></span> <span data-ttu-id="902f3-118">Bu bayrak, tüm ACL 'ler kökle aynıysa alt ağacın ACL ouput 'sini atlar.</span><span class="sxs-lookup"><span data-stu-id="902f3-118">This flag skips the acl ouput of subtree if all it's acls are same as the root.</span></span>

## <span data-ttu-id="902f3-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="902f3-119">PARAMETERS</span></span>

### <span data-ttu-id="902f3-120">-Hesap</span><span class="sxs-lookup"><span data-stu-id="902f3-120">-Account</span></span>
<span data-ttu-id="902f3-121">Dosya sistemi işlemini yürütme</span><span class="sxs-lookup"><span data-stu-id="902f3-121">The Data Lake Store account to execute the filesystem operation in</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="902f3-122">-Eşzamanlılık</span><span class="sxs-lookup"><span data-stu-id="902f3-122">-Concurrency</span></span>
<span data-ttu-id="902f3-123">Paralel olarak işlenen dosya/dizinlerin sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="902f3-123">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="902f3-124">Varsayılan, sistem belirtimine göre en iyi çaba olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="902f3-124">Default will be computed as a best effort based on system specification.</span></span>

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

### <span data-ttu-id="902f3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="902f3-125">-DefaultProfile</span></span>
<span data-ttu-id="902f3-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="902f3-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="902f3-127">-GetAcl</span><span class="sxs-lookup"><span data-stu-id="902f3-127">-GetAcl</span></span>
<span data-ttu-id="902f3-128">ACL 'yi kök yoldan başlayarak alır</span><span class="sxs-lookup"><span data-stu-id="902f3-128">Retrieves the acl starting from the root path</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAllProperties, GetAclDump
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="902f3-129">-GetDiskUsage</span><span class="sxs-lookup"><span data-stu-id="902f3-129">-GetDiskUsage</span></span>
<span data-ttu-id="902f3-130">Kök yolundan başlayarak disk kullanımını alır</span><span class="sxs-lookup"><span data-stu-id="902f3-130">Retrieves the disk usage starting from the root path</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetDiskUsage, GetAllProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="902f3-131">-Hide, tentacl</span><span class="sxs-lookup"><span data-stu-id="902f3-131">-HideConsistentAcl</span></span>
<span data-ttu-id="902f3-132">ACL 'Ler tüm alt ağaçta aynıysa dizin alt ağacını gösterin.</span><span class="sxs-lookup"><span data-stu-id="902f3-132">Do not show directory subtree if the ACLs are the same throughout the entire subtree.</span></span> <span data-ttu-id="902f3-133">Bu, yalnızca ACL 'Lerin farklı yollarını görmeyi kolaylaştırır. Örneğin,/a/b altındaki tüm dosyalar ve klasörler aynıysa, üst bölümü/a/b altında göstermeyin ve uyumlu ACL 'deki yalnızca ' true ' ile çıktı/a/b, dosyalar için ACL 'ler alınmadan belirlenemediğinden, ıncludefiles ayarlanmamış olabilir.</span><span class="sxs-lookup"><span data-stu-id="902f3-133">This makes it easier to see only the paths up to which the ACLs differ.For example if all files and folders under /a/b are the same, do not show the subtreeunder /a/b, and just output /a/b with 'True' in the Consistent ACL columnCannot be set if IncludeFiles is not set, because consistent Acl cannot be determined without retrieving acls for the files.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAllProperties, GetAclDump
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="902f3-134">-Includefile</span><span class="sxs-lookup"><span data-stu-id="902f3-134">-IncludeFile</span></span>
<span data-ttu-id="902f3-135">Dosya düzeyinde istatistikleri göster (varsayılan olarak yalnızca dizin düzeyindeki bilgiler gösterilir)</span><span class="sxs-lookup"><span data-stu-id="902f3-135">Show stats at file level (default is to show directory-level info only)</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="902f3-136">-MaximumDepth</span><span class="sxs-lookup"><span data-stu-id="902f3-136">-MaximumDepth</span></span>
<span data-ttu-id="902f3-137">Kök dizininden, disk kullanımı veya ACL 'nin görüntülendiği en yüksek derinlik</span><span class="sxs-lookup"><span data-stu-id="902f3-137">Maximum depth from the root directory till which disk usage or acl is displayed</span></span>

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

### <span data-ttu-id="902f3-138">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="902f3-138">-OutputPath</span></span>
<span data-ttu-id="902f3-139">Çıkış dosyasının yolu.</span><span class="sxs-lookup"><span data-stu-id="902f3-139">Path to output file.</span></span> <span data-ttu-id="902f3-140">Yerel bir yol veya adl yolu olabilir.</span><span class="sxs-lookup"><span data-stu-id="902f3-140">Can be a Local path or Adl Path.</span></span> <span data-ttu-id="902f3-141">Varsayılan olarak, yereldir.</span><span class="sxs-lookup"><span data-stu-id="902f3-141">By default it is local.</span></span> <span data-ttu-id="902f3-142">Kaydettoadl belirtilmezse, aynı hesaptaki bir ADL yolu olur</span><span class="sxs-lookup"><span data-stu-id="902f3-142">If SaveToAdl is pecified then it is an ADL path in the same account</span></span>

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

### <span data-ttu-id="902f3-143">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="902f3-143">-PassThru</span></span>
<span data-ttu-id="902f3-144">Silme işleminin sonucunu belirten bir Boole yanıtının döndürülmesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="902f3-144">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="902f3-145">-Yol</span><span class="sxs-lookup"><span data-stu-id="902f3-145">-Path</span></span>
<span data-ttu-id="902f3-146">Belirtilen Data Lake hesabındaki yol.</span><span class="sxs-lookup"><span data-stu-id="902f3-146">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="902f3-147">'/Folder/file.txt ' biçiminde bir dosya veya klasör olabilir; burada DNS, ilk '/', dosya sisteminin kökünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="902f3-147">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="902f3-148">-SaveToAdl</span><span class="sxs-lookup"><span data-stu-id="902f3-148">-SaveToAdl</span></span>
<span data-ttu-id="902f3-149">Geçmişse, döküm dosyasını ADL 'ye kaydeder.</span><span class="sxs-lookup"><span data-stu-id="902f3-149">If passed then saves the dump file to ADL.</span></span>
<span data-ttu-id="902f3-150">Bu durumda, DumpFile WIL bir ADL yolu olmalıdır</span><span class="sxs-lookup"><span data-stu-id="902f3-150">The DumpFile wil be a ADL path in that case</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="902f3-151">-Onay</span><span class="sxs-lookup"><span data-stu-id="902f3-151">-Confirm</span></span>
<span data-ttu-id="902f3-152">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="902f3-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="902f3-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="902f3-153">-WhatIf</span></span>
<span data-ttu-id="902f3-154">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="902f3-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="902f3-155">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="902f3-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="902f3-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="902f3-156">CommonParameters</span></span>
<span data-ttu-id="902f3-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="902f3-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="902f3-158">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="902f3-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="902f3-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="902f3-159">INPUTS</span></span>

### <span data-ttu-id="902f3-160">System. String</span><span class="sxs-lookup"><span data-stu-id="902f3-160">System.String</span></span>

### <span data-ttu-id="902f3-161">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="902f3-161">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="902f3-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="902f3-162">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="902f3-163">System. Int32</span><span class="sxs-lookup"><span data-stu-id="902f3-163">System.Int32</span></span>

## <span data-ttu-id="902f3-164">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="902f3-164">OUTPUTS</span></span>

### <span data-ttu-id="902f3-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="902f3-165">System.Boolean</span></span>

## <span data-ttu-id="902f3-166">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="902f3-166">NOTES</span></span>

## <span data-ttu-id="902f3-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="902f3-167">RELATED LINKS</span></span>
