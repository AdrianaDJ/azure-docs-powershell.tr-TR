---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/export-azdatalakestorechilditemproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
ms.openlocfilehash: 25615684db8b78a461b39b1a8cfc159d42a56883
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095989"
---
# <span data-ttu-id="61926-101">Export-AzDataLakeStoreChildItemProperty</span><span class="sxs-lookup"><span data-stu-id="61926-101">Export-AzDataLakeStoreChildItemProperty</span></span>

## <span data-ttu-id="61926-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61926-102">SYNOPSIS</span></span>
<span data-ttu-id="61926-103">Belirtilen yoldaki tüm ağacın (disk kullanımı ve ACL) bir çıkış yoluna dışarı aktarır</span><span class="sxs-lookup"><span data-stu-id="61926-103">Exports the properties (Disk usage and Acl) for the entire tree from the specified path to a output path</span></span>

## <span data-ttu-id="61926-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="61926-104">SYNTAX</span></span>

### <span data-ttu-id="61926-105">GetDiskUsage</span><span class="sxs-lookup"><span data-stu-id="61926-105">GetDiskUsage</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="61926-106">GetAllProperties</span><span class="sxs-lookup"><span data-stu-id="61926-106">GetAllProperties</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-GetAcl] [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61926-107">GetAclDump</span><span class="sxs-lookup"><span data-stu-id="61926-107">GetAclDump</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>] [-GetAcl]
 [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="61926-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="61926-108">DESCRIPTION</span></span>
<span data-ttu-id="61926-109">**Export-AzDataLakeStoreChildItemProperty** , verilen dizin için ADLS alanı kullanımı veya/ve ACL kullanımını raporlamak üzere kullanılır ve alt dizinleri ve dosyaları.</span><span class="sxs-lookup"><span data-stu-id="61926-109">The **Export-AzDataLakeStoreChildItemProperty** is used to report the ADLS space usage or/and ACL usage for the given directory and it's sub directories and files.</span></span>

## <span data-ttu-id="61926-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="61926-110">EXAMPLES</span></span>

### <span data-ttu-id="61926-111">Örnek 1: tüm alt dizinler ve dosyalar için disk kullanımı ve ACL kullanımını alma</span><span class="sxs-lookup"><span data-stu-id="61926-111">Example 1: Get the disk usage and ACL usage for all subdirectories and files</span></span>
```
PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -GetDiskUsage -IncludeFile
```

<span data-ttu-id="61926-112">/A'in altındaki tüm alt dizinler ve dosyalar için disk kullanımı ve ACL kullanımını edinin.</span><span class="sxs-lookup"><span data-stu-id="61926-112">Get the disk usage and ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="61926-113">Includefile, dosyaların Ayrıca</span><span class="sxs-lookup"><span data-stu-id="61926-113">IncludeFile ensures the usage is reported for files also</span></span>

### <span data-ttu-id="61926-114">Örnek 2: tutarlı ACL 'ye sahip tüm alt dizinlerin ve dosyaların ACL kullanımını alma</span><span class="sxs-lookup"><span data-stu-id="61926-114">Example 2: Get the ACL usage for all subdirectories and files with the consistent ACL hidden</span></span>
```
PS C:\> $fullAcl="user:contoso-userid:--x|user::rwx|other::---|group::rwx"
PS C:\> $newFullAcl = $fullAcl.Split("{|}");
PS C:\> Set-AzDataLakeStoreItemAcl -Account ContosoADL -Path /a -Acl $newFullAcl -Recurse -Debug

PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -HideConsistentAcl -IncludeFile
```

<span data-ttu-id="61926-115">Tüm alt dizinlerin ve/A'in altındaki dosyaların ACL kullanımını edinin.</span><span class="sxs-lookup"><span data-stu-id="61926-115">Get the ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="61926-116">Includefile, dosyaların da bu şekilde raporlanmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="61926-116">IncludeFile ensures the usage is reported for files also.</span></span> <span data-ttu-id="61926-117">Bu durumda Hidelıtentacl, tüm alt öğelerin/aile aynı ACL 'e sahip olduğu için, alt öğelerin ACL 'sini gösterir.</span><span class="sxs-lookup"><span data-stu-id="61926-117">HideconsistentAcl in this case will show the Acl of /a, not it's children since all of the children has same acl as /a.</span></span> <span data-ttu-id="61926-118">Bu bayrak, tüm ACL 'ler kökle aynıysa alt ağacın ACL çıkışını atlar.</span><span class="sxs-lookup"><span data-stu-id="61926-118">This flag skips the acl output of subtree if all it's acls are same as the root.</span></span>

## <span data-ttu-id="61926-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="61926-119">PARAMETERS</span></span>

### <span data-ttu-id="61926-120">-Hesap</span><span class="sxs-lookup"><span data-stu-id="61926-120">-Account</span></span>
<span data-ttu-id="61926-121">Dosya sistemi işlemini yürütme</span><span class="sxs-lookup"><span data-stu-id="61926-121">The Data Lake Store account to execute the filesystem operation in</span></span>

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

### <span data-ttu-id="61926-122">-Eşzamanlılık</span><span class="sxs-lookup"><span data-stu-id="61926-122">-Concurrency</span></span>
<span data-ttu-id="61926-123">Paralel olarak işlenen dosya/dizinlerin sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="61926-123">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="61926-124">Varsayılan, sistem belirtimine göre en iyi çaba olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="61926-124">Default will be computed as a best effort based on system specification.</span></span>

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

### <span data-ttu-id="61926-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61926-125">-DefaultProfile</span></span>
<span data-ttu-id="61926-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="61926-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61926-127">-GetAcl</span><span class="sxs-lookup"><span data-stu-id="61926-127">-GetAcl</span></span>
<span data-ttu-id="61926-128">ACL 'yi kök yoldan başlayarak alır</span><span class="sxs-lookup"><span data-stu-id="61926-128">Retrieves the acl starting from the root path</span></span>

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

### <span data-ttu-id="61926-129">-GetDiskUsage</span><span class="sxs-lookup"><span data-stu-id="61926-129">-GetDiskUsage</span></span>
<span data-ttu-id="61926-130">Kök yolundan başlayarak disk kullanımını alır</span><span class="sxs-lookup"><span data-stu-id="61926-130">Retrieves the disk usage starting from the root path</span></span>

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

### <span data-ttu-id="61926-131">-Hide, tentacl</span><span class="sxs-lookup"><span data-stu-id="61926-131">-HideConsistentAcl</span></span>
<span data-ttu-id="61926-132">ACL 'Ler tüm alt ağaçta aynıysa dizin alt ağacını gösterin.</span><span class="sxs-lookup"><span data-stu-id="61926-132">Do not show directory subtree if the ACLs are the same throughout the entire subtree.</span></span> <span data-ttu-id="61926-133">Bu, yalnızca ACL 'Lerin farklı yollarını görmeyi kolaylaştırır. Örneğin,/a/b altındaki tüm dosyalar ve klasörler aynıysa, üst bölümü/a/b altında göstermeyin ve uyumlu ACL 'deki yalnızca ' true ' ile çıktı/a/b, dosyalar için ACL 'ler alınmadan belirlenemediğinden, ıncludefiles ayarlanmamış olabilir.</span><span class="sxs-lookup"><span data-stu-id="61926-133">This makes it easier to see only the paths up to which the ACLs differ.For example if all files and folders under /a/b are the same, do not show the subtreeunder /a/b, and just output /a/b with 'True' in the Consistent ACL columnCannot be set if IncludeFiles is not set, because consistent Acl cannot be determined without retrieving acls for the files.</span></span>

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

### <span data-ttu-id="61926-134">-Includefile</span><span class="sxs-lookup"><span data-stu-id="61926-134">-IncludeFile</span></span>
<span data-ttu-id="61926-135">Dosya düzeyinde istatistikleri göster (varsayılan olarak yalnızca dizin düzeyindeki bilgiler gösterilir)</span><span class="sxs-lookup"><span data-stu-id="61926-135">Show stats at file level (default is to show directory-level info only)</span></span>

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

### <span data-ttu-id="61926-136">-MaximumDepth</span><span class="sxs-lookup"><span data-stu-id="61926-136">-MaximumDepth</span></span>
<span data-ttu-id="61926-137">Kök dizininden, disk kullanımı veya ACL 'nin görüntülendiği en yüksek derinlik</span><span class="sxs-lookup"><span data-stu-id="61926-137">Maximum depth from the root directory till which disk usage or acl is displayed</span></span>

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

### <span data-ttu-id="61926-138">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="61926-138">-OutputPath</span></span>
<span data-ttu-id="61926-139">Çıkış dosyasının yolu.</span><span class="sxs-lookup"><span data-stu-id="61926-139">Path to output file.</span></span> <span data-ttu-id="61926-140">Yerel bir yol veya adl yolu olabilir.</span><span class="sxs-lookup"><span data-stu-id="61926-140">Can be a Local path or Adl Path.</span></span> <span data-ttu-id="61926-141">Varsayılan olarak, yereldir.</span><span class="sxs-lookup"><span data-stu-id="61926-141">By default it is local.</span></span> <span data-ttu-id="61926-142">SaveToAdl belirtilmezse, bu, aynı hesaptaki bir ADL yoludur</span><span class="sxs-lookup"><span data-stu-id="61926-142">If SaveToAdl is specified then it is an ADL path in the same account</span></span>

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

### <span data-ttu-id="61926-143">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="61926-143">-PassThru</span></span>
<span data-ttu-id="61926-144">Silme işleminin sonucunu belirten bir Boole yanıtının döndürülmesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="61926-144">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="61926-145">-Yol</span><span class="sxs-lookup"><span data-stu-id="61926-145">-Path</span></span>
<span data-ttu-id="61926-146">Belirtilen Data Lake hesabındaki yol.</span><span class="sxs-lookup"><span data-stu-id="61926-146">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="61926-147">'/Folder/file.txt ' biçiminde bir dosya veya klasör olabilir; burada DNS, ilk '/', dosya sisteminin kökünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="61926-147">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

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

### <span data-ttu-id="61926-148">-SaveToAdl</span><span class="sxs-lookup"><span data-stu-id="61926-148">-SaveToAdl</span></span>
<span data-ttu-id="61926-149">Geçmişse, döküm dosyasını ADL 'ye kaydeder.</span><span class="sxs-lookup"><span data-stu-id="61926-149">If passed then saves the dump file to ADL.</span></span>
<span data-ttu-id="61926-150">Bu durumda, DumpFile WIL bir ADL yolu olmalıdır</span><span class="sxs-lookup"><span data-stu-id="61926-150">The DumpFile wil be a ADL path in that case</span></span>

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

### <span data-ttu-id="61926-151">-Onay</span><span class="sxs-lookup"><span data-stu-id="61926-151">-Confirm</span></span>
<span data-ttu-id="61926-152">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="61926-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61926-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61926-153">-WhatIf</span></span>
<span data-ttu-id="61926-154">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="61926-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61926-155">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="61926-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61926-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61926-156">CommonParameters</span></span>
<span data-ttu-id="61926-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="61926-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61926-158">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61926-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61926-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="61926-159">INPUTS</span></span>

### <span data-ttu-id="61926-160">System. String</span><span class="sxs-lookup"><span data-stu-id="61926-160">System.String</span></span>

### <span data-ttu-id="61926-161">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="61926-161">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="61926-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="61926-162">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="61926-163">System. Int32</span><span class="sxs-lookup"><span data-stu-id="61926-163">System.Int32</span></span>

## <span data-ttu-id="61926-164">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="61926-164">OUTPUTS</span></span>

### <span data-ttu-id="61926-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="61926-165">System.Boolean</span></span>

## <span data-ttu-id="61926-166">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="61926-166">NOTES</span></span>

## <span data-ttu-id="61926-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="61926-167">RELATED LINKS</span></span>
