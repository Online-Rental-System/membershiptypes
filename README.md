# membershiptypes

public int MembershipTypes(MembershipTypes mt)
{
  try
  {
    SqlCommand cmd = new SqlCommand("sp_membershiptypes",con);
    cmd.CommandType = CommandType.StoredProcedure;
    cmd.Parameters.AddWidthValue("@id",mt.Id);
    cmd.Parameters.AddWidthValue("@name",mt.Name);
    con.Open();
    int Result = cmd.ExecuteNonQuery();
    cmd.Dispose();
    con.Close();
    return result;  
  }
  catch
  {
    throw;
  }
}

public int AddMembershipTypes(MembershipTypes mt)
{
  try
  {
    SqlCommand cmd = new SqlCommand("sp_addmembershiptypes",con);
    cmd.CommandType = CommandType.StoredProcedure;
    cmd.Parameters.AddWidthValue("@id",mt.Id);
    cmd.Parameters.AddWidthValue("@name",mt.Name);
    con.Open();
    int Result = cmd.ExecuteNonQuery();
    cmd.Dispose();
    con.Close();
    return result;  
  }
  catch
  {
    throw;
  }
}
